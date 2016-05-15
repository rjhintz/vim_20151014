# Vim Lab
## Tips
*  `q:` command line history
*  `:verbose` display where a value was last set. Ex: `:verbose set history`
*  Get `solarized light` by using `set background light` and `let g:airline_theme='solarized'`

## Plug In Manager
### Vundle
[Vundle](https://github.com/VundleVim/Vundle.vim)

## Status Line
### Airline
[Airline](https://github.com/vim-airline/vim-airline)

#### How to Configure
* [How to configure to look like screenshot](http://vi.stackexchange.com/questions/5622/how-to-configure-vim-airline-plugin-to-look-like-its-own-project-screenshot)
* Help `:h airline`

```
:verbose set statusline
statusline=%!airline#statusline(1)
        Last set from ~/.vim/bundle/vim-airline/autoload/airline.vim
```

```
vim-airline doesn't appear until I create a new split
    Add set laststatus=2 to your vimrc
```

## Tabbing
### Supertab
[ervandew/supertab](https://github.com/ervandew/supertab)

### Old / Deprecated
#### 20151014
Add ons for VIM
* install zsch
* get .zshrc from (https://github.com/Integralist/ProVim/blob/master/.zshrc)
* Change shell `chsh -s /bin/zsh`
* Restart so that new sheel is effective
* Ruby not installed
* Install RVM. See (https://rvm.io/rvm/install)
* Install RVM stable with Ruby `\curl -sSL https://get.rvm.io | bash -s stable --ruby`
```
○ gpg --keyserver hkp://keys.gnupg.net --recv-keys 409B6B1796C275462A1703113804BB82D39DC0E3
gpg: directory `/home/rjhintz/.gnupg' created
gpg: new configuration file `/home/rjhintz/.gnupg/gpg.conf' created
gpg: WARNING: options in `/home/rjhintz/.gnupg/gpg.conf' are not yet active during this run
gpg: keyring `/home/rjhintz/.gnupg/secring.gpg' created
gpg: keyring `/home/rjhintz/.gnupg/pubring.gpg' created
gpg: requesting key D39DC0E3 from hkp server keys.gnupg.net
gpg: /home/rjhintz/.gnupg/trustdb.gpg: trustdb created
gpg: key D39DC0E3: public key "Michal Papis (RVM signing) <mpapis@gmail.com>" imported
gpg: no ultimately trusted keys found
gpg: Total number processed: 1
gpg:               imported: 1  (RSA: 1)
get_ruby_version:1: command not found: ruby                                  

M. ~ 
○ \curl -sSL https://get.rvm.io | bash -s stable --ruby
]1; rjhintz: Downloading https://github.com/rvm/rvm/archive/1.26.11.tar.gz
Downloading https://github.com/rvm/rvm/releases/download/1.26.11/1.26.11.tar.gz.asc
gpg: Signature made Mon 30 Mar 2015 02:52:13 PM PDT using RSA key ID BF04FF17
gpg: Good signature from "Michal Papis (RVM signing) <mpapis@gmail.com>"
gpg: WARNING: This key is not certified with a trusted signature!
gpg:          There is no indication that the signature belongs to the owner.
Primary key fingerprint: 409B 6B17 96C2 7546 2A17  0311 3804 BB82 D39D C0E3
     Subkey fingerprint: 62C9 E5F4 DA30 0D94 AC36  166B E206 C29F BF04 FF17
GPG verified '/home/rjhintz/.rvm/archives/rvm-1.26.11.tgz'

Installing RVM to /home/rjhintz/.rvm/
    Adding rvm PATH line to /home/rjhintz/.profile /home/rjhintz/.mkshrc /home/rjhintz/.bashrc /home/rjhintz/.zshrc.
    Adding rvm loading line to /home/rjhintz/.profile /home/rjhintz/.bash_profile /home/rjhintz/.zlogin.
Installation of RVM in /home/rjhintz/.rvm/ is almost complete:

  * To start using RVM you need to run `source /home/rjhintz/.rvm/scripts/rvm`
    in all your open shell windows, in rare cases you need to reopen all shell windows.

# Rich Hintz,
#
#   Thank you for using RVM!
#   We sincerely hope that RVM helps to make your life easier and more enjoyable!!!
#
# ~Wayne, Michal & team.

In case of problems: http://rvm.io/help and https://twitter.com/rvm_io
rvm 1.26.11 (latest) by Wayne E. Seguin <wayneeseguin@gmail.com>, Michal Papis <mpapis@gmail.com> [https://rvm.io/]
Searching for binary rubies, this might take some time.
No binary rubies available for: ubuntu/15.04/x86_64/ruby-2.2.1.
Continuing with compilation. Please read 'rvm help mount' to get more information on binary rubies.
Checking requirements for ubuntu.
Installing requirements for ubuntu.
Updating systemrjhintz password required for 'apt-get --quiet --yes update': 
............
Installing required packages: gawk, libreadline6-dev, zlib1g-dev, libssl-dev, libyaml-dev, libsqlite3-dev, sqlite3, autoconf, libgdbm-dev, libncurses5-dev, automake, libtool, bison, libffi-dev...............
Requirements installation successful.
Found user configured '-j' flag in 'rvm_make_flags', please note that RVM can detect number of CPU threads and set the '-j' flag automatically if you do not set it.
Installing Ruby from source to: /home/rjhintz/.rvm/rubies/ruby-2.2.1, this may take a while depending on your cpu(s)...
ruby-2.2.1 - #downloading ruby-2.2.1, this may take a while depending on your connection...
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100 12.7M  100 12.7M    0     0  8931k      0  0:00:01  0:00:01 --:--:-- 8932k
ruby-2.2.1 - #extracting ruby-2.2.1 to /home/rjhintz/.rvm/src/ruby-2.2.1....
ruby-2.2.1 - #applying patch /home/rjhintz/.rvm/patches/ruby/2.2.1/fix_installing_bundled_gems.patch.
ruby-2.2.1 - #configuring.........................................................
ruby-2.2.1 - #post-configuration..
ruby-2.2.1 - #compiling...............................................................................
ruby-2.2.1 - #installing................
ruby-2.2.1 - #making binaries executable..
ruby-2.2.1 - #downloading rubygems-2.4.8
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100  437k  100  437k    0     0   659k      0 --:--:-- --:--:-- --:--:--  658k
No checksum for downloaded archive, recording checksum in user configuration.
ruby-2.2.1 - #extracting rubygems-2.4.8....
ruby-2.2.1 - #removing old rubygems.........
ruby-2.2.1 - #installing rubygems-2.4.8......................
ruby-2.2.1 - #gemset created /home/rjhintz/.rvm/gems/ruby-2.2.1@global
ruby-2.2.1 - #importing gemset /home/rjhintz/.rvm/gemsets/global.gems...............................................
ruby-2.2.1 - #generating global wrappers........
ruby-2.2.1 - #gemset created /home/rjhintz/.rvm/gems/ruby-2.2.1
ruby-2.2.1 - #importing gemsetfile /home/rjhintz/.rvm/gemsets/default.gems evaluated to empty gem list
ruby-2.2.1 - #generating default wrappers........
ruby-2.2.1 - #adjusting #shebangs for (gem irb erb ri rdoc testrb rake).
Install of ruby-2.2.1 - #complete 
Ruby was built without documentation, to build it run: rvm docs generate-ri
Creating alias default for ruby-2.2.1...

  * To start using RVM you need to run `source /home/rjhintz/.rvm/scripts/rvm`
    in all your open shell windows, in rare cases you need to reopen all shell windows.
get_ruby_version:1: command not found: ruby        
```

`source ~/.rvm/scripts/rvm`  <--add this to zsch config
##20151015
`cp ~/ProVim/.vimrc ~/.vimrc`
```
○ vim
Error detected while processing /home/rjhintz/.vimrc:
line  119:
E117: Unknown function: pathogen#infect
E15: Invalid expression: pathogen#infect()
line  124:
E185: Cannot find color scheme 'Tomorrow-Night'
Press ENTER or type command to continue
```
[Install Pathogen package manager](http://www.vim.org/scripts/script.php?script_id=2332)
```
mkdir -p ~/.vim/autoload ~/.vim/bundle 
curl -LSso ~/.vim/autoload/pathogen.vim https://tpo.pe/pathogen.vim
```

Comment out (using '#') color theme in line 124

Add to top of `.vimrc`
```
set runtimepath+=~/.vim/config
runtime basic.vim
runtime plugins.vim
runtime bindings.vim
```

Stray characters appear and movement through the file doesn't work as expected.

--------------------------
##References
[Pro Vim](https://www.safaribooksonline.com/library/view/pro-vim/9781484202500/)

