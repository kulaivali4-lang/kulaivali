class ATM:
  def __init__(self):
    self.pin = ' '
    self.balance = 1000
    self.menu()

  def menu(self):
      print('''
      1) enter 1 to create pin.
      2) press 2 to cash withdrawl.
      3) press 3 to cash deposit.
      4) press 4 to cash transfer.
      5) press 5 to  change pin.
      6) press 6 to exit.
      ''')
      user_choice = input("Please enter your choice:")

      if user_choice == '1':
       self.create_pin()

  def create_pin(self):
        ask1 = input("enter your pin:")
        self.pin == ask1
        print("pin created successfully")
        self.menu()

  def withdrawl(self):
    ask2 = input("enter your pin:")
    if ask2 == self.pin:
     amount = int(input("enter the amount to withdrawl:"))

     if amount <= self.balance:
      print('insufficient balance') 
      self.menu()

    else:
     self.balance = self.balance - amount
     print('please collect your cash',amount,'you are left with,', self.balance)
     self.menu()

     #change pin
     def change_pin(self):
      old_pin = input("enter your old pin:")
      if old_pin == self.pin:
        ask3 = input("enter your new pin:")
        self.pin = ask3
        print("pin changed successfully")
        self.menu()
      else:
        print("invalid pin")
        self.menu()
