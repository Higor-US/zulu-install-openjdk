# 1° - SET UP THE AZUL APT REPOSITORY:

[install the necessary dependencies]

sudo apt-get q update
sudo apt-get -yq install gnupg curl

[add Azul's public key]

sudo apt-key adv \
  --keyserver hkp://keyserver.ubuntu.com:80 \
  --recv-keys 0xB1998361219BD9C9
  
 [download and install the package that adds ]
 [the Azul APT repository to the list of sources]

curl -O https://cdn.azul.com/zulu/bin/zulu-repo_1.0.0-3_all.deb

[install the package]

sudo apt-get install ./zulu-repo_1.0.0-3_all.deb

[update the package sources]

sudo apt-get update

# 2° - WHEN THE REPOSITORY IS SET UP, INSTALL THE REQUIRED AZUL ZULU PACKAGE BY RUNNING apt-get install <package>.
(For example, to install Azul Zulu JDK 11, run)

[install Azul Zulu JDK 11]
  
sudo apt-get install zulu11-jdk

# 3° - TO VERIFY YOUR INSTALLATION, RUN THE java -version COMMAND

$ java -version
openjdk version "11.0.10" 2021-01-19 LTS
OpenJDK Runtime Environment Zulu11.45+27-CA (build 11.0.10+9-LTS)
OpenJDK 64-Bit Server VM Zulu11.45+27-CA (build 11.0.10+9-LTS, mixed mode)
