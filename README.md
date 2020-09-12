# Send
CTGU自动报平安

### Github Actions
取消.github/workflow/autosend.yml, 第16行的注释  
   
config.txt文件中按示例添加用户信息  
如用户不需要接收邮件，将该用户的邮箱地址设为“null”即可
  
仓库首页 Settings -> Secrets -> New secret, 添加邮件发送方信息  
name与.github/workflow/autosend.yml, 第43、44行一致: FROMEMAIL、POP3KEY  
value即发送方邮箱地址和POP3、SMTP授权码  

### 本地  
clone仓库到本地  

本地安装Python，进入仓库目录，使用“pip install -r requirements.txt”安装所需依赖文件  
推荐使用virtualvenv建立虚拟环境  

send.py -f <发送方邮箱地址> -k <邮箱授权码>  
