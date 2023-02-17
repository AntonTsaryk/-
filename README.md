#42
class Person:
    def __init__(self, name, age):
        self.name = name
        self.age = age

    def display(self):
        print("Person name : ", self.name)
        print("Person age = ", self.age)

class Student(Person):
    def __init__(self, name, age, section):
        Person.__init__(self, name, age)
        self.section = section

    def displayStudent(self):
        print("Student name : ", self.name)
        print("Student age = ", self.age)
        print("Student section = ", self.section)

P = Person("Anton", 13)
P.display()
print("-------------------------------")
S = Student("Sasha", 15, "Mathematics")
S.displayStudent()

#43
class BankAccount:
  def __init__(self, accountNumber, name, balance):
    self.accountNumber = accountNumber
    self.name = name
    self.balance = balance

  def Deposit(self, d):
    self.balance = self.balance + d

  def Withdrawal(self, w):
    if (self.balance < w):
      print("Хлопче, в тебе мало грошей")
    else:
      self.balance = self.balance - w

  def bankFees(self):
    self.balance = (95 / 100) * self.balance

  def display(self):
    print("Account Number : ", self.accountNumber)
    print("Account Name : ", self.name)
    print("Account Balance : ", self.balance, " $")

newAccount = BankAccount(2178514584, "Anton", 25)
newAccount.Withdrawal(15)
newAccount.Deposit(10)
newAccount.display()
