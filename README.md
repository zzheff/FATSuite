# FATSuite
A tool for quick identify vulnerable targets



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
注：首次进入时，如未安装会自动识别系统及chrome版本并下载解压（安装好的路径会在“setting”界面显示）

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

<img width="480" alt="Pasted image 20221129130145" src="https://user-images.githubusercontent.com/103415470/204598729-1378cab8-0a6d-49b6-9940-4f0b3fcdabee.png">

会自动为域名添加http和https

<img width="555" alt="Pasted image 20221129182300" src="https://user-images.githubusercontent.com/103415470/204598147-c836489e-7e50-4b12-91d4-3d21b3cd9ce9.png">



### 开始检测：

<img width="555" alt="image" src="https://user-images.githubusercontent.com/103415470/204610396-ac064b20-4969-4a33-91fb-3860424b7576.png">


点击“check”跳到检测结果显示页面


![3241670052978_ pic](https://user-images.githubusercontent.com/103415470/205438065-1580b910-2d09-4e84-baa0-bdf0c1613231.jpg)


当在终端看到以下信息时，就表示截图已经完成，chromedriver的进程也已经关闭（截图会比获取网站信息慢一些）

<img width="338" alt="image" src="https://user-images.githubusercontent.com/103415470/205439422-f638ae48-c96b-4e42-87d3-8d9811d67905.png">




### 缩略图：


![3251670065547_ pic](https://user-images.githubusercontent.com/103415470/205438075-e29bc017-6986-4a04-b112-37c155a0d3ac.jpg)



