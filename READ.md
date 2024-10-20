코더 : [이대현]

리뷰어 : [권 미 경]

---

🔑 **PRT(Peer Review Template)**

[o]  **1. 주어진 문제를 해결하는 완성된 코드가 제출되었나요?**
- 문제에서 요구하는 최종 결과물이 첨부
- import random
class Account:

  count = 0
  #count+=1

  def __init__(self, depositor, initial_b):
    self.bank = "SC은행"
    #self.depositor = input("예금주를 입력하시오")
    #self.initial_b = int(input("잔s액을 입력하시오"))
    self.depositor = depositor
    self.initial_b = initial_b
    self.account_number = self.account_generator()
    self.deposit_count = 0

    Account.count+=1 #2. 계좌 객체의 개수를 지정하고, 계좌 객체 개수 증가


  def account_generator(self):
    num1 = random.randint(100, 999)
    num2 = random.randint(10,99)
    num3 = random.randint(100000,999999)
    return f"{num1}-{num2}-{num3}"

  # 3. Account 클래스로부터 생성된 계좌의 개수를 출력
  def get_account_num(cnt):
    # print(Account.count)
    return cnt.count

  # 4. 입금 메서드
  def deposit(self, inputmoney):
    if int(inputmoney) >=1: #입금은 최소 1원 이상
      self.balance += inputmoney
      self.deposit_count += 1
      # 7. 입금 5회시 이자 지급
      if self.deposit_count % 5 == 0:
        self.initial_b *= 1.01 # 1% 이자

  # 5. 출금
  def withdraw(self, inputmoney):
    if inputmoney <= self.balance: #잔고 이하일 때만 출금
      self.balance -= inputmoney
      # ??
    else:
      print("No remained money!!")

  # 6.
  def display_info(self):
    print("은행이름:{}, 예금주:{}, 계좌번호:{}, 잔고:{}원".format(self.bank,self.depositor,self.account_number,self.balance))

  # 10. 입금과 출금 내역이 기록되도록 코드를 업데이트
  def deposit_history(self):
    print("")
    
[o]  **2. 전체 코드에서 가장 핵심적이거나 가장 복잡하고 이해하기 어려운 부분에 작성된 

	- 잘 작성되었다고 생각되는 부분을 캡쳐해 근거로 첨부
  def __init__(self, depositor, initial_b):
    self.bank = "SC은행"
    #self.depositor = input("예금주를 입력하시오")
    #self.initial_b = int(input("잔s액을 입력하시오"))
    self.depositor = depositor
    self.initial_b = initial_b
    self.account_number = self.account_generator()
    self.deposit_count = 0

    Account.count+=1 #2. 계좌 객체의 개수를 지정하고, 계좌 객체 개수 증가
        
[o]  **3. 에러가 난 부분을 디버깅하여 문제를 “해결한 기록"을 남겼거나 "새로운 시도 
또는 추가 실험"을 수행해봤나요?**
- 문제 원인 및 해결 과정을 잘 작성되었다고 생각되는 부분을 캡쳐해 근거
---------------------------------------------------------------------------
TypeError                                 Traceback (most recent call last)
<ipython-input-11-0ac3ce2149d0> in <cell line: 1>()
----> 1 deposit=Account()
      2 deposit.account_generator()

TypeError: Account.__init__() missing 2 required positional arguments: 'depositor' and 'initial_b'
        
[x]  **4. 회고를 잘 작성했나요?**


[o]  **5. 코드가 간결하고 효율적인가요?**
 -  잘 작성되었다고 생각되는 부분을 캡쳐해 근거로 첨부
# 4. 입금 메서드
  def deposit(self, inputmoney):
    if int(inputmoney) >=1: #입금은 최소 1원 이상
      self.balance += inputmoney
      self.deposit_count += 1
      # 7. 입금 5회시 이자 지급
      if self.deposit_count % 5 == 0:
        self.initial_b *= 1.01 # 1% 이자

---
### 참고 문헌
