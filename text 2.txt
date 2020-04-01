#Ques2

a=eval(input())
def new(b):
  try:
    for k in b:
      if type(b[k])==type({}):
        for i in b[k]:
          b[k+i]=b[k][i]
        b.pop(k)
        new(b)
    else:
      print(b)
  except RuntimeError:
    pass
new(a)
