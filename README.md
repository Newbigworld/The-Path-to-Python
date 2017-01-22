***The-Path-to-Python***

# 一、元素分类
    li = [11,22,33,44,55,66,77,88,99,100,101]
    dic = {'k1':[],'k2':[]}
    for i in li:
      if i >=66:
        dic['k1'].append(i)
      else:
        dic['k2'].append(i)
    print(dic)
