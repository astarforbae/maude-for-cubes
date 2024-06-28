# Maude for Cubes

（未完成）本项目旨在使用Maude对二阶/三阶魔方进行自动求解。
（状态空间太大，目前只能求解简单的情况，详见RESULTS.pdf）

## 使用步骤

仅在Linux环境下测试过。

`rubkis-cube.maude` 和 `pocket-cube.maude` 分别对应二阶魔方和三阶魔方求解的Maude文件。

两个文件的结构几乎一致，仅导入的文件和初始状态有些许不同，下面以`rubiks-cube.maude`为例说明使用步骤。

1. 将该文件第一行导入的文件路径改为你自己的`model-checker.maude`文件路径；
2. 修改`init`的值为你想要求解的魔方状态；（状态定义参考`RESULTS.pdf`和`STATE-DEFINITION.png`）；
3. 运行：
```bash
/path/to/your/maude rubiks-cube.maude
```
即可看到结果。

