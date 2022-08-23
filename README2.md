
### 画图中文乱码解决

中文字体库拷贝至：/opt/conda/lib/python3.9/site-packages/matplotlib/mpl-data/fonts/ttf/SimHei.ttf

修改配置文件：/opt/conda/lib/python3.9/site-packages/matplotlib/matplotlibrc

```
font.family:SimHei,  sans-serif
```

### 通过临时重写配置文件的方法，可以解决 Matplotlib 显示中文乱码的问题

代码如下所示：

```
import matplotlib.pyplot as plt
plt.rcParams["font.sans-serif"]=["SimHei"] #设置字体
plt.rcParams["axes.unicode_minus"]=False #该语句解决图像中的“-”负号的乱码问题
```

将上述代码添加到您的绘图程序中，即可解决中文乱码的问题。这是一种非常灵活、便捷的解决方法。

### NotebookApp now is deprecated, use ServerApp instead

https://github.com/stefanproell/jupyter-notebook-docker-compose/issues/2
