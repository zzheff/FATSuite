# FATSuite
A tool for quick identify vulnerable targets



![logo](https://user-images.githubusercontent.com/103415470/205480533-87a59a9f-40e1-4bb3-9c4b-5c3f512aeb96.jpg)


## 20230203更新：

新增功能：

1.导出为CSV
<img width="1136" alt="image" src="https://user-images.githubusercontent.com/103415470/216507023-74fcc56a-fab8-4100-85cf-2f0cd4ae3668.png">

2.指纹识别

指纹库是Finger的，师傅们可以自行在plugin中增加
<img width="1146" alt="image" src="https://user-images.githubusercontent.com/103415470/216521531-f54b913d-685e-47aa-a2a1-e072dad58f02.png">


3.JsFinder插件 

注：
运行JsFinder需要有Python环境
<img width="1136" alt="image" src="https://user-images.githubusercontent.com/103415470/216506911-f2dfe6ce-bebd-4320-9651-73f714773b97.png">

<img width="829" alt="image" src="https://user-images.githubusercontent.com/103415470/216506874-4b397e2f-2291-416c-9a0d-503aa7fcf716.png">


4.目录爆破
<img width="1136" alt="image" src="https://user-images.githubusercontent.com/103415470/216506720-e194a6d2-29f0-4fd3-8e07-2f5c0abd121c.png">

可选后缀：
<img width="962" alt="image" src="https://user-images.githubusercontent.com/103415470/216506783-b3a65e5b-cf7f-4913-a4f7-71a51ade75c2.png">


<img width="596" alt="image" src="https://user-images.githubusercontent.com/103415470/216501918-dbc24e48-0f9c-46b5-80d6-8d5b6596cd00.png">
可以提前选择需要排除的状态码
如需每次自动加载，请在StatusCode.txt文件中写入



## 工具产生背景：

项目中通过Hunter、FOFA和Zoomeye获取到的资产较多且信息有滞后性。用oneforall等工具收集到的资产较多但信息不足。

且所有获取到的资产都需要逐个访问，花费一些不必要的时间，所以想有一款工具导入目标资产后，可以直接获取目标当下的页面截图、IP、IP地理位置、CIDR、状态码、中间件并自定义Title关键字进行筛选，这样可以更快速的定位薄弱目标。



## 使用方法：
```
java -jar FATSuite.jar
```

当windows添加了中文语言包时，请运行如下命令：
```
java -Dfile.encoding=utf-8 -jar FATSuite.jar
```

## 使用说明：


### 环境检查：
点击“Check”检查是否安装chromedriver

注：首次进入时，如未安装Windows会自动下载最新版本ChromeDriver并解压，Mac下载后需用户手动双击解压（安装好的路径会在“setting”界面显示）
注：如Linux运行截图失败，请查看ChromeDriver是否有执行权限

<img width="694" alt="image" src="https://user-images.githubusercontent.com/103415470/204596714-d3808aad-203f-49b6-b9b1-72f401904d7b.png">



### 前台页面：
点击“Enter”进入主页面

<img width="695" alt="image" src="https://user-images.githubusercontent.com/103415470/204596896-de959669-f3f1-40e9-a96b-55850c2683ed.png">



### 设置：
进入主页面后可以通过点击setting设置UA、线程、超时时间以及关键字（用于匹配特定的URL Title）

<img width="693" alt="image" src="https://user-images.githubusercontent.com/103415470/204597107-6407cd29-3e87-4be4-80ec-0ba4e016eb17.png">


setting页面中显示的是默认设置，如果要添加关键字可以在文件keywords.txt文件中逐行添加

<img width="700" alt="image" src="https://user-images.githubusercontent.com/103415470/204597247-62b46a76-2fdf-4bf1-bab8-295da3488a84.png">


首次运行会自动检测keywords.txt，没有的话会自动创建
如果临时添加关键字，可直接在关键字界面输入，以英文`,`（逗号）分割。

<img width="600" alt="image" src="https://user-images.githubusercontent.com/103415470/204607880-85917ccb-41bd-4468-a6d6-a9b127347a68.png">
设置好后点击Apply应用，完成自定义设置。



### 导入检测文件：
点击“import”选择要检查的目标文件，必须是txt文件，选择后会在界面显示

<img width="555" alt="Pasted image 20221129182243" src="https://user-images.githubusercontent.com/103415470/204597945-32b53072-76c2-4c22-b1bb-378d9751086f.png">

示例：目标文件中的URL

<img width="475" alt="image" src="https://user-images.githubusercontent.com/103415470/205480361-860929a8-211a-461d-a09e-17bce5ded814.png">

会自动为域名添加http和https




### 开始检测：

<img width="552" alt="image" src="https://user-images.githubusercontent.com/103415470/205480367-26bdd960-5c6a-4d06-a062-6b3684840255.png">


点击“check”跳到检测结果显示页面


![3261670140224_ pic](https://user-images.githubusercontent.com/103415470/205480154-80cf2924-111f-435c-8cd9-07c6ede46923.jpg)



当在终端看到以下信息时，就表示截图已经完成，chromedriver的进程也已经关闭（截图会比获取网站信息慢一些）

<img width="338" alt="image" src="https://user-images.githubusercontent.com/103415470/205439422-f638ae48-c96b-4e42-87d3-8d9811d67905.png">




### 缩略图：

通过缩略图用户可从海量资产中准确获取薄弱目标，比如获取登录页面、未识别出的cms等其他信息。

![3271670140355_ pic](https://user-images.githubusercontent.com/103415470/205480159-5bade0f7-9c82-458e-b5d4-6c0d743184c9.jpg)


## 改进：
Linux和Mac会根据Chrome的版本下载ChromeDriver



