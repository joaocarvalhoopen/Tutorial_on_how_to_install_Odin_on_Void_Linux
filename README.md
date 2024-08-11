# Tutorial on how to install Odin on Void Linux
Void Linux is a great distribution and this is how to install the latest Odin version on it.

## Description

```
# Install the nonfree repo for VSCode and debug repo for the debug stuff. 
sudo xbps-install -S void-repo-nonfree
sudo xbps-install -S void-repo-debug

# Install git and the base development package.
sudo xbps-install -S git
sudo xbps-install -S base-devel

# Install the LLVM18 stuff.
sudo xbps-install -S llvm18
sudo xbps-install -S llvm18-dbg
sudo xbps-install -S libllvm18-dbg
sudo xbps-install -S llvm18-cross-tools
sudo xbps-install -S llvm18-doc

# Install the CLANG18 stuff.
sudo xbps-install -S clang18
sudo xbps-install -S clang-dbg

mkdir odin

cd odin

# Clone and compile Odin.

git clone https://github.com/odin-lang/Odin.git

cd Odin

make release

pwd

# Add the path of Odin to the PATH variable ./bashrc:
export PATH="$PATH:/home/joao/odin/Odin"

```

## Now install OLS and VSCode


```
# Clone and compile OLS

git clone https://github.com/DanielGavin/ols.git

cd ols

./build.sh

pwd

# Add the path of ols to the PATH variable ./bashrc:
export PATH="$PATH:/home/joao/odin/ols"


# Install vscode in the form of code-oss 

sudo xbps-install -S vscode

# Insert the alias of code-oss to code in ./bashrc:
alias code='/usr/lib/code-oss/bin/code-oss'

mkdir ~/test

cd ~/test

code .

# Install plugin Odin Language from Daniel Gavin for VSCode.

# Install plugin CodeLLDB for the debugger of CLANG in VSCode.

# Install plugin Error Lens for showing the errors of Odin inline with the source code line.

```

And now have lots of fun programming in Odin!

## Have fun!
Best regards,
João Carvalho
