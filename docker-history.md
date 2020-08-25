    1  clear
    2  sudo apt-get update
    3  sudo apt-get -y install \ apt-transport-https \ ca-certificates \ curl \ gnupg-agent \ software-properties-common
    4  exit
    5  clear
    6  sudo apt-get -y install   apt-transport-https   ca-certificates   curl   gnupg-agent   software-properties-common
    7  curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
    8  sudo apt-key fingerprint 0EBFCD88
    9  sudo add-apt-repository    "deb [arch=amd64] https://download.docker.com/linux/ubuntu \
   10     $(lsb_release -cs) \
   11  sudo add-apt-repository    "deb [arch=amd64] https://download.docker.com/linux/ubuntu    $(lsb_release -cs) 
   12  sudo add-apt-repository    "deb [arch=amd64] https://download.docker.com/linux/ubuntu \
   13     $(lsb_release -cs) \
   14     stable"
   15  sudo apt-get update
   16  sudo apt-get install -y docker-ce=5:18.09.5~3-0~ubuntu-bionic docker-ce-cli=5:18.09.5~3-0~ubuntu-bionic containerd.io
   17  sudo usermod -a -G docker cloud_user
   18  exit
   19  clear
   20  docker run hello-world
   21  clear
   22  docker info
   23  clear
   24  docker --version
   25  docker run hello-world
   26  clear
   27  docker run nginx:1.15.11
   28  docker run busybox
   29  docker run busybox echo hello world!
   30  docker run -d --name nginx --restart unless-stopped -p 8080:80 --memory 500M --memory-reservation 256M nginx
   31  docker ps
   32  docker ps -a
   33  docker container stop nginx
   34  docker container start nginx
   35  docker container stop nginx
   36  docker container rm nginx
   37  docker ps -a
   38  docker ps
   39  docker run -d --name nginx --restart unless-stopped -p 8080:80 --memory 500M --memory-reservation 256M nginx
   40  docker ps
   41  curl localhost:8080
   42  docker ps -a
   43  docker container stop nginx
   44  docker ps -a
   45  docker container start nginx
   46  docker container rm hello-world
   47  docker container stop nginx
   48  docker rm nginx
   49  #upgrade to previous version
   50  history
   51  history >> history.txt
   52  ls
   53  vim history.txt
   54  sudo yum install git
   55  sudo apt-get install git
   56  mkdir docker
   57  cd docker/
   58  ls
   59  touch README.md
   60  ls
   61  git init
   62  git add -A
   63  git commit -m "initialize repo
   64  "
   65  git config --global docker.blocksom@gmaio.com
   66  git config --global General-Docker
   67  git config --global config --global user.email docker.blocksom@gmail.com
   68  git remote add origin https://github.com/General-Docker/docker-dca-prep.git
   69  git push -u origin master
   70  git remote add origin https://github.com/General-Docker/docker-dca-prep.git
   71  git push -u origin master
   72  git commit -m ""
   73  git config user.email docker.blocksom@gmail.com
   74  git config user.name General-Docker
   75  git commit -m ""
   76  git commit -m "."
   77  src refspec master does not match any.src refspec master does not match any.
   78  git remote add origin https://github.com/General-Docker/docker-dca-prep.git
   79  git push -u origin master
   80  sed man
   81  man sed
   82  cd ..
   83  ls
   84  sed '100' history.txt 
   85  sed -n '100' history.txt 
   86  clear
   87  #upgrading docker engine
   88  docker version
   89  #first downgrade
   90  sudo systemctl stop docker
   91  sudo apt-get remove -y docker-ce docker-ce-cli
   92  docker sudo apt-get update
   93  sudo apt-get update
   94  sudo apt-get install -y docker-ce=5:18.09.4~3-0~ubuntu-bionic docker-ce-cli=5:18.09.4~3-0~ubuntu-bionic
   95  docker version
   96  #that's how to downgrade
   97  sudo apt-get install -y docker-ce=5:18.09.5~3-0~ubuntu-bionic docker-ce-cli=5:18.09.5~3-0~ubuntu-bionic
   98  docker version
   99  #end of lesson
  100  history
  101  #Configuring Logging Drivers(Splunk, Journald, etc.)
  102  docker info | grep Logging
  103  sudo vim /etc/default/grub
  104  sudo update-grub
  105  docker info | grep Logging
  106  sudo vi /etc/docker/daemon.json
  107  sudo systemctl restart docker
  108  docker run --log-driver json-file --log-opt max-size=50m nginx
  109  #Logging drivers are a pluggable framework for accessing log data from services and containers in Docker
  110  docker info | grep Logging
  111  history
  112  #end of lesson on Configuring Logging Drivers
  113  history >> docker-history.md
