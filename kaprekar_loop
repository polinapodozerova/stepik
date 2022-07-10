def kaprekar_step(L):
    return (int(''.join(map(str, sorted(L)[::-1]))) - int(''.join(map(str, sorted(L)))))

def numerics(n):
    return [int(i) for i in str(n)]

def kaprekar_check(n):
    l = len(numerics(n))
    return not (n in [100, 1000, 100000] or len(set(numerics(n))) == 1 or l not in [3, 4, 6])
      
def kaprekar_loop(n):
    if kaprekar_check(n):
        history = []
        n_prev = 0
        while n_prev != n:
            history.append(n)
            n_prev = n
            print(n)
            n = kaprekar_step(numerics(n))
            if n in history and n != n_prev:
                print(f'Следующее число - {n}, кажется процесс зациклился...')
                break
    else:
        print(f'Ошибка! На вход подано число {n}, не удовлетворяющее условиям процесса Капрекара')
