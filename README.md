# GeoDjango
#### 安装python gdal 
``` 
下载： https://www.lfd.uci.edu/~gohlke/pythonlibs/
$ pip install GDAL-2.3.3-cp36-cp36m-win_amd64.whl


```

#### windows安装 gdal 
```
安装 gdal-201-1500-x64-core.msi
配置环境变量后  重启
    Path:C:\Program Files\GDAL
    GDAL_DATA:C:\Program Files\GDAL\gdal-data
    GDAL_DRIVER_PATH:C:\Program Files\GDAL\gdalplugins
验证是否安装成功
cmd gdalinfo --version 
```

####  OSGeo4W
```
在setting添加
if os.name == 'nt':
    import platform
    OSGEO4W = r"C:\OSGeo4W"
    if '64' in platform.architecture()[0]:
        OSGEO4W += "64"
    assert os.path.isdir(OSGEO4W), "Directory does not exist: " + OSGEO4W
    os.environ['OSGEO4W_ROOT'] = OSGEO4W
    os.environ['GDAL_DATA'] = OSGEO4W + r"\share\gdal"
    os.environ['PROJ_LIB'] = OSGEO4W + r"\share\proj"
    os.environ['PATH'] = OSGEO4W + r"\bin;" + os.environ['PATH']
OSGeo4W可以不安装，直接copy文件即可
 
```

