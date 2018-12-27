# Academic Hosting 101 

A short guide about how to host your academic websites using [Jekyll](https://jekyllrb.com/).

## Creating simple, powerful websites and hosting them for free.

As an academic, its a common need to share information about your portfolio, or your class, or your next reading group. In this tutorial, we will use a very simple program, [Jekyll](https://jekyllrb.com/) to create such websites and host them free on Github using [Github Pages](https://pages.github.com/). Then, we will explore several off-the-shelf themes to make your website look good. Finally, we will cover one popular theme [al-folio](https://github.com/alshedivat/al-folio) using which you can share your portfolio as well as maintain a list of publications with your already exisiting bibtex.

## Installations

First, let us install the required tools in your system. 

### Install Jekyll

Jekyll is a Ruby Gem which can be [installed](https://jekyllrb.com/docs/installation/) in most systems. Ruby is a scripting language which powers the website builder toolkit Jekyll. Follow the instructions based on your system of choice:

#### Linux or Mac

1. Install Ruby Version Manager ([RVM](http://rvm.io/)). Open a Terminal (Control + Alt + T) and type the following commands:

```
gpg2 --recv-keys 409B6B1796C275462A1703113804BB82D39DC0E3 7D2BAF1CF37B13E2069D6956105BD0E739499BDB
```
and

```
\curl -sSL https://get.rvm.io | bash -s stable --rails
```

2. Install Ruby. Here we will use the version `2.3.1`

```
rvm install 2.3.1
```

3. Now that Ruby is installed, you can proceed to install Jekyll based on the system:

3.1 For Mac

Copy paste the following:

a. Installs required dependencies to install Jekyll

```
xcode-select --install
```

b. Install the Jekyll Gem

```
gem install --user-install bundler jekyll
```

c. Open your bash config file. Its the file called `.bashrc` which is located in the home directory. You can edit the file using any editor of choice, here we will use `nano`. Type in the Terminal:

```
nano ~/.bashrc
```

This will open the file in your Terminal itself. Scroll down to the very end, and paste these two lines:

```
export GEM_HOME=$HOME/gems
export PATH=$HOME/gems/bin:$PATH
```

For more information / reference, [check this doc](https://jekyllrb.com/docs/installation/macos/).

3.2 For Ubuntu

a. Make sure you have the required dependencies for Jekyll. Copy paste the following in your Terminal.

```
sudo apt-get install build-essential zlib1g-dev
```

b. Remember you already installed Ruby from the previous step. Now we just need to install the Jekyll Gem, which is the same procedure as for Mac:

```
gem install jekyll bundler
```

Thats it! You can also [refer this document](https://jekyllrb.com/docs/installation/ubuntu/) for alternative ways to install.


#### Windows

1. Install [RubyInstaller](https://rubyinstaller.org/downloads/), which will take care of the installation of Ruby. Download the top executable: `Ruby+Devkit 2.5.3-1 (x64)`. Run and install.

2. Once installed, open a new command prompt, and type the following:

```
gem install jekyll bundler
```

This should install Jekyll and necessary files.  If you need more information, refer to [this document](https://jekyllrb.com/docs/installation/windows/).

### Install Git

