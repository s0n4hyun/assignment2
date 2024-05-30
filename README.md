string_ = "월요일, 화요일, 수요일, 목요일, 금요일, 토요일, 일요일"

# 쉼표와 공백을 기준으로 문자열을 분할하여 각 요일을 얻습니다.
days = string_.split(", ")

# 각 요일을 축약한 버전을 만듭니다.
abbreviated_days = [day[:3] for day in days]

# 축약된 요일을 '|' 구분자로 결합합니다.
weekdays = "|".join(abbreviated_days)

print(weekdays)  # 출력: 월|화|수|목|금|토|일




def sum_of_numbers_between(a, b):
    # a와 b 중에서 작은 값과 큰 값을 구합니다.
    start = min(a, b)
    end = max(a, b)
    
    # start부터 end까지의 모든 자연수를 더합니다.
    total = sum(range(start, end + 1))
    
    return total

# 사용자로부터 두 개의 자연수를 입력받습니다.
num1 = int(input("첫 번째 자연수를 입력하세요: "))
num2 = int(input("두 번째 자연수를 입력하세요: "))

# 두 수 사이의 모든 자연수의 합을 계산합니다.
result = sum_of_numbers_between(num1, num2)

print(f"{num1}부터 {num2}까지의 모든 자연수의 합은 {result}입니다.")



# 주어진 리스트
numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]

# 짝수를 필터링하여 새로운 리스트 생성
even_numbers = filter(lambda x: x % 2 == 0, numbers)

# 각 짝수의 제곱을 계산하여 새로운 리스트 생성
even_squares = map(lambda x: x ** 2, even_numbers)

# 결과 출력
print(list(even_squares))  # 출력: [4, 16, 36, 64, 100]
