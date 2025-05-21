# Banking-program-using-Python
def show_balance():
  print("____________________________________")
  print(f"your balance is Rs {balance:.2f}")
  print("____________________________________")

def deposit():
  amount = float(input("Enter amount to deposit: "))
  
  if amount < 0:
    print("Invalid amount")
    return 0
  else:
    return amount

def withdraw():
  amount = float(input("Enter amount to withdraw: "))
  
  if amount < 0 :
    print("Amount should be greater than zero")
    return 0
  elif amount > balance:
    print("Insufficient balance")
    return 0
  else:
    return amount

def main():
 balance = 0
 is_running = True

 while is_running:
  print("___________________________________")
  print("Banking")
  print("1. Show balance")
  print("2. Deposit")
  print("3. Withdraw")
  print("4. Exit")
  print("____________________________________")

  choice = input("Enter your choice: ")

  if choice == "1":
    show_balance()
  elif choice == "2":
    balance += deposit()
  elif choice == "3":
    balance -= withdraw()
  elif choice == "4":
    is_running = False
  else:
    print("Invalid choice")

  print("....THANKYOU....")

if __name__ == "__main__":
  main()
