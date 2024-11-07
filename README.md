# Atividade 1 - Verificação de Números Primos

## Objetivo:
Implementar uma função em Python que verifica se um número é primo.

## Como proceder:
1. Implemente a função `is_prime` no arquivo `primos.py`.
2. Teste seu código com os exemplos fornecidos.
3. Faça o commit das alterações e envie o código para o GitHub.

## Exemplos de teste:
```python
print(is_prime(2))   # True
print(is_prime(3))   # True
print(is_prime(4))   # False
print(is_prime(11))  # True
print(is_prime(15))  # False
```
---
---
def is_prime(n):
    if n <= 1:
        return False
    if n <= 3:
        return True
    if n % 2 == 0 or n % 3 == 0:
        return False
    i = 5
    while i * i <= n:
        if n % i == 0 or n % (i + 2) == 0:
            return False
        i += 6
    return True

# Exemplos de teste
print(is_prime(2))   # True
print(is_prime(3))   # True
print(is_prime(4))   # False
print(is_prime(11))  # True
print(is_prime(15))  # False
