1. 搜索死锁
```maude
search init =>! S:State .
```

2. load file 

```maude
load /home/ZhangXingYi/local/maude/model-checker.maude .
load triple.maude .
load neighbor.maude .
load cube.maude .
```

```maude
load /home/ZhangXingYi/local/maude/model-checker.maude .
load double.maude .
load neighbor-2.maude .
load cube-2.maude .
```


3. 查找是否存在饥饿

```maude
red modelCheck(init, []<> eatingPhi(1)) .
red modelCheck(init, [](hungryPhi(1) -> <> eatingPhi(1))) .
red modelCheck(init, ([]<> hungryPhi(1) )-> ([]<> eatingPhi(1))) .
red modelCheck(init, ([]<> hungryPhi(N) )-> ([]<> eatingPhi(N))) .
```