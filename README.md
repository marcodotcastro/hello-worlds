# Hello Worlds
## Configurações

- Objetivo fazer o upgrade e o downgrade da version default
 - Ruby
   - Instalar por Apt
     - sudo apt install ruby 
   - Executar Hello World
     - ruby hello.rb
   - Instalar por Manager Version, https://rvm.io/
     - Pré-configuração
       - /
     - Instalar manager
       - \curl -sSL https://get.rvm.io | bash -s stable     
     - Instalar versão
       - rvm list known
       - rvm install 2.6
    - Executar Hello World
      - ruby hello.rb
    
 - PHP
   - Instalar por Apt
     - sudo apt install php
   - Executar Hello World
     - php hello.php
   - Instalar por Manager Version, https://phpbrew.github.io/phpbrew/
     - Pré-configuração
       - sudo apt install php-bz2 libxml2-dev libbz2-dev libxslt-dev libzip-dev libssl-dev libreadline-dev
     - Instalar manager
       - curl -L -O https://github.com/phpbrew/phpbrew/releases/latest/download/phpbrew.phar
       - chmod +x phpbrew.phar
       - sudo mv phpbrew.phar /usr/local/bin/phpbrew
       - phpbrew init
       - [[ -e ~/.phpbrew/bashrc ]] && source ~/.phpbrew/bashrc
     - Instalar versão
       - phpbrew known
       - phpbrew install 5.4.0 +default
    - Executar Hello World
      - php hello.php
    
 - Java
   - Instalar por Apt
     - sudo apt install openjdk-8-jdk
   - Executar Hello World
     - javac hello.java
     - java HelloWorld
   - Instalar por Manager Version, https://www.jenv.be/
     - Pré-configuração
       - /
     - Instalar manager
       - git clone https://github.com/jenv/jenv.git ~/.jenv
       - echo 'export PATH="$HOME/.jenv/bin:$PATH"' >> ~/.bashrc
       - echo 'eval "$(jenv init -)"' >> ~/.bashrc
       - source ~/.bashrc
     - Instalar versão
       - jenv versions
       - jenv doctor
       - which java
       - ls -la /usr/bin/java
       - ls -la /etc/alternatives/java
       - jenv add /usr/lib/jvm/java-11-openjdk-amd64
       - jenv global 1.8
    - Executar Hello World
      - javac hello.java
      - java HelloWorld
    
    
 - Javascript
   - Instalar por Apt
     - sudo apt install nodejs 
   - Executar Hello World
     - nodejs hello.js
   - Instalar por Manager Version, https://github.com/nvm-sh/nvm
     - Pré-configuração
       - /
     - Instalar manager
       - curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.35.3/install.sh | bash   
     - Instalar versão
       - nvm ls-remote
       - nvm install 14.7.0
       - nvm exec 14 node -v 
    - Executar Hello World
      - nvm exec 14 node hello.js
 
 - Python
   - Instalar por Apt
     - sudo apt install python3-pip
   - Executar Hello World
     - python3 hello.py
   - Instalar por Manager Version, https://github.com/pyenv/pyenv
     - Pré-configuração
       - /
     - Instalar manager
       - git clone https://github.com/pyenv/pyenv.git ~/.pyenv
       - echo 'export PYENV_ROOT="$HOME/.pyenv"' >> ~/.bashrc
       - echo 'export PATH="$PYENV_ROOT/bin:$PATH"' >> ~/.bashrc
       - eval "$(pyenv init -)"
     - Instalar versão
       - pyenv install --list
       - pyenv install 3.7.8
       - pyenv shell 3.7.8
       - python3 --version
    - Executar Hello World
      - python3 hello.py
