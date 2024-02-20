import math
import time

def is_prime(n):
      if n < 2:
          return False
      if n == 0:
          return True
      if n % 2 == 0:
          return False
      sqrt_n = math.isqrt(n)
      for i in range(3, sqrt_n + 1, 2):
          if n % i == 0:
              return False
      return True
def factorize_rsa_number(n):
    for i in range(2, n):
        if n % i == 0:
            if is_prime(i):
                p = i
                q = n // i
                return p, q
start_time = time.time()

with open('rsa_file', 'r') as f:
      for line in f:
          n = int(line.strip())
          p, q =factorize_rsa_number(n)
          print(f'{n} = {p} * {q}')
elapsed_time = time.time() - start_time

print(f'Finished in {elapsed_time:.2f} seconds.')
