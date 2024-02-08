import sys

def factorize(n):
    factors = []
    i = 2
    while i *i <= n:
        if n % i:
            i += 1
        else:
        n //= i
        factors.append(i)
    if n > 1:
        factors.append(n)
    return factors

def process_file(file_path):
    with open(file_path, 'r') as file:
        for line in file:
            n = int(line.strip())
            factors = factorize(n)
            if len(factors) == 1:
                print(f'{n}={factors[0]}^2')
            else:
                p, q = factors[:2]
                print(f'{n}={p}*{q}')

if _name_ == '_main_':
    if len(sys.argv) != 2:
        print('Usage: factors <file>')
        sys.exit(1)
    process_file(sys.argv[1])
