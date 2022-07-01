#소수 만들기

from itertools import combinations


def is_prime_num(num):
    if num == 0 or num == 1:
        return False
    else:
        for n in range(2, (num // 2) + 1):
            if num % n == 0:
                return False

        return True


def solution(nums):
    answer = 0
    array = list(combinations(nums, 3))
    for n in array:
        if is_prime_num(sum(n)) == True:
            answer += 1

    return answer

#print(solution([1,2,3,4]))
