# AIFFEL Campus Online Code Peer Review Templete
- 코더 : 김지영 신상호
- 리뷰어 : 이익현


# PRT(Peer Review Template)
- [ ]  **1. 주어진 문제를 해결하는 완성된 코드가 제출되었나요?** 네
     # @title 기본 제목 텍스트
def find_min_max(numbers):

    # min_value와 max_value 변수를 초기화
    min_value = float('inf') # min_value는 양의 무한대(float('inf'))로 초기화하여 어떤 숫자보다도 큰 값으로 설정
    max_value = float('-inf') # max_value는 음의 무한대(float('-inf'))로 초기화하여 어떤 숫자보다도 작은 값으로 설정

    def update_min_max(num):
      nonlocal min_value, max_value # 외부함수의 변수인 min_value, max_value 참조
      if num < min_value:
        min_value = num # 만약 num 값이 min_value보다 작다면 min_value를 num 값으로 변경
      if num > max_value:
        max_value = num
      if num <= min_value: # 만약 num 값이 max_value보다 크다면 max_value를 num 값으로 변경
        min_value = num

    for num in numbers: # numbers 리스트의 모든 값을 순환하며 최댓값과 최솟값 업데이트
        update_min_max(num)

    def get_min(): # 최솟값을 반환하는 내부함수
      return min_value

    def get_max(): # 최댓값을 반환하는 내부함수
      return max_value

    return (get_min, get_max)  # 외부함수는 내부함수(get_min()과 get_max())를 반환

    
- [ ]  **2. 전체 코드에서 가장 핵심적이거나 가장 복잡하고 이해하기 어려운 부분에 작성된 
주석 또는 doc string을 보고 해당 코드가 잘 이해되었나요?**
    #입력받은 fn 의 이름을 fn_name 으로 문자열로 assign
    #  print( type(fn_name) )  #제대로 string 으로 출력되는 것 확인함
    #fn 의 실행횟수를 알려주는 integar 형식의 count 변수, initial 0로 설정
  이런주석들을 보며 더 잘이해할수있었다
        
- [ ]  **3. 에러가 난 부분을 디버깅하여 문제를 해결한 기록을 남겼거나
새로운 시도 또는 추가 실험을 수행해봤나요?**
    print( type(fn_name) )  #제대로 string 으로 출력되는 것 확인함
        
- [ ]  **4. 회고를 잘 작성했나요?**
    
        - 회고 에 배운점 느낀점등 잘 기록되있었다
        
- [ ]  **5. 코드가 간결하고 효율적인가요?**
  간결하고 주석을 써서 이해하기 쉽게 되있다 생각한다


# 회고(참고 링크 및 코드 개선)
다른조가 한거를 보면서 내가 못했던 부분을 참고를 할수있어서 도움이되었고 , 파이썬이 어렵다고 느꼇다.
