# py
import string
import random 

def dp():

  length = int(input("Enter the desired password length: "))
  p = pg(length)
  print("Generated password:", p)

def pg(length):

  c = string.ascii_letters + string.digits + string.punctuation
  p = ''.join(random.choice(c) for _ in range(length))
  return p
  
if _name_ == "_main_":
  dp()
