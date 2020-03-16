lives = 3
word = ""
result = ""
diff = 0
chars = 0

def print_line(list):
  s = ""
  for i in list:
    s+=i
  print(s)
def get_char():
  s = ""
  s = input("Enter symbol: ")
  if len(s) == 1:
    return s
  while len(s) > 1:
    s = input("Enter only 1 symbol: ")
  return s
def init_game():
  global chars
  global word
  global result
  global diff
  word = input("Enter word:")
  l = len(word)
  chars = l
  while l > 0:
    result+="|_|"
    l-=1
  result = list(result)
  while diff == 0:
    diff = int(input("Enter game level:(1,2,3)"))
    if diff < 0 or diff > 3:
      diff = 0
      print("Too hard..))")
def start_game():
  global word
  global result
  global chars
  global lives
  while chars >= 0:
    if chars == 0:
      print("You win and save your life<3")
      return 0
    print_line(result)
    if lives == 0:
      print("YOU LOOOSER!!!")
      return 0
    j = 1
    c = get_char()
    if c in word:
      print("Thats right dude!")
      for i in word:
        if i == c:
          chars-=1
          result[j-1] = ""
          result[j] = c
          result[j+1] = ""
        j+=3
    else:
      lives-=1
      print("There is no such letter:P")



init_game()
start_game()
print_line(result)
