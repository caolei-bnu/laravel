# laravel-for MacOS

1.composer和laravel的安装与配置：  
  
Composer 是 PHP 的一个依赖管理工具。我们可以在项目中声明所依赖的外部工具库，Composer 会帮你安装这些依赖的库文件，有了它，我们就可以很轻松的使用一个命令将其他人的优秀代码引用到我们的项目中来。  
Composer 默认情况下不是全局安装，而是基于指定的项目的某个目录中（例如 vendor）进行安装。  
Composer 需要 PHP 5.3.2+ 以上版本，且需要开启 openssl。  
  
用homebrew安装composer：  
brew install composer  
用composer 安装laravel：  
composer global require laravel/installer  
valet install  

安装后的composer通常在 ~/.composer/vendor/bin/ 路径下  
cd ~/.composer/vendor/bin/   
配置composer：  
vi ~/.bash_profile  
添加path到.bash_profile:  
export PATH=${PATH}:/Users/caolei/.composer/vendor/bin/  
sourse ~/.bash_profile  
如果在下面生成新框架的时候出现了链接超时的情况：  
需要换一个国内的镜像  
composer config -g repo.packagist composer https://packagist.phpcomposer.com  
  
  
2.生成一个laravel的框架  
  
建一个新的目录：mkdir ~/WEB/  
在该目录下用laravel生成一个新的框架：（juglans是框架名）  
composer create-project --prefer-dist laravel/laravel juglans  
此时出现了juglans目录，在WEB目录下：  
valet park  
cd juglans  
php artisan serve  
将生成的地址（通常是127.0.0.1:8000）复制到浏览器中，即可看到我们的框架  
最后由于laravel的框架中有一些谷歌字体需要从外网下载  
可以查找google然后把其中字体的部分全删了  
