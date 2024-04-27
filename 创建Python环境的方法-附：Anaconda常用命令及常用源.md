# 创建Python环境的方法（附：Anaconda常用命令及常用源）

## 一、创建python环境的方法

### 1. 使用python进行创建环境

1. 创建虚拟环境

```powershell
python -m venv ENV-NAME   # ENV-NAME:表示创建的虚拟环境的名称
```

2. 激活虚拟环境

```python
ENV-NAME\Scripts\activate  # ENV-NAME:表示创建的虚拟环境的名称
```

3. 退出虚拟环境

```powershell
deactivate
```

### 2. 使用anaconda进行创建环境

1. 创建虚拟环境

```powershell
conda create -n ENV-NAME python=x.x   # ENV-NAME:表示创建环境的名称;  x.x:表示创建虚拟环境的python版本
```

2. 激活（或切换）虚拟环境

```powershell
conda activate ENV-NAME   # ENV-NAME:表示创建的虚拟环境的名称
```

3. 退出虚拟环境

```powershell
conda deactivate
```

## 二、Anaconda的常用命令

1. 查看创建的所有虚拟环境

```powershell
conda env list
```

2. 查看当前环境下的所有包

```powershell
conda list
```

3. 更新当前的conda

```powershell
conda update conda
```

4. 删除虚拟环境下的某个包

```powershell
conda remove --name ENV-NAME PACKAGE-NAME     # ENV-NAME:表示创建的虚拟环境的名称; PACKAGE-NAME:表示要删除包的名称
```

5. 删除虚拟环境

```powershell
conda remove -n ENV-NAME --all  # ENV-NAME:表示创建的虚拟环境的名称
```

6. 下载包

```powershell
# 第一种方式: 直接下载
conda install PACKAGE-NAME   #  PACKAGE-NAME:表示要下载的包的名称

# 第二种方式: 指定下载源
conda install -c ORIGIN PACKAGE-NAME   # ORIGIN: 表示下载源;  PACKAGE-NAME:表示要下载的包的名称
```

> python的下载包的方式：
>
> ```powershell
> # 第一种方式: 直接下载
> pip install PACKAGE-NAME    # PACKAGE-NAME:表示要下载的包的名称
> # 第二种方式: 指定下载源
> pip install PACKAGE-NAME -i ORIGIN    # ORIGIN: 表示下载源;  PACKAGE-NAME:表示要下载的包的名称
> ```

## 三、常用的源

1. 豆瓣源

```powershell
https://pypi.doubanio.com/simple/       
```

2.  清华源 

```powershell
https://pypi.tuna.tsinghua.edu.cn/simple
```

3. 中国科学技术大学源 

```powershell
https://pypi.mirrors.ustc.edu.cn/simple/
```