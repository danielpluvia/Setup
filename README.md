# Solutions

* Issue: [How to fix Arduino serial port bug on MAC OS SIERRA](https://www.youtube.com/watch?v=wyocdvAKo64&t=11s)
* Solution: Install "CH34x_Install_V1.3.pkg"

# [macOS Setup Guide](https://sourabhbajaj.com/mac-setup)

# Tools

* [iTerm2](https://www.iterm2.com/)

  * oh-my-zsh
    * Custom Configuration
      - https://gist.github.com/kevin-smets/8568070
    * Theme
      * [Pure](https://github.com/sindresorhus/pure)
      * [Theme_Snazzy](https://github.com/sindresorhus/terminal-snazzy)
      * [Powerlevel9k](https://github.com/bhilburn/powerlevel9k)
    * Plugins
      * [zsh-syntax-highlighting](https://github.com/zsh-users/zsh-syntax-highlighting)
      * [autojump](https://github.com/wting/autojump)
      * [zsh-autosuggestions](https://github.com/zsh-users/zsh-autosuggestions)
    * [Powerline](https://github.com/powerline/fonts)

* Java

  * [Install java by Homebrew](https://medium.com/@at_ishikawa/install-java-by-homebrew-on-mac-d99aff457c1f)

    * Java 9

      * ```brew cask install java```

    * Install Java8

      * ```bash
        brew tap caskroom/versions
        brew cask install java8
        ```

    * Optional

      * [jEnv](http://www.jenv.be/)

  * [Setup](https://medium.com/microsoftazure/setting-up-a-macbook-pro-mac-os-x-high-sierra-for-java-and-azure-cloud-development-ca5d60ed79ba)

    * Use IntelliJ IDEA CE

    * ```bash
      $ brew cask info intellij-idea-ce
      intellij-idea-ce: 2017.3.4,173.4548.28
      ...
      $ brew cask install intellij-idea-ce
      ```

    * Do Not Use NetBeans IDE 8.2

      * [not working with java9](https://stackoverflow.com/questions/46476470/cant-create-project-on-netbeans-8-2)

      * Install

      * ```bash
        $ brew cask info netbeans-java-ee
        netbeans-java-ee: 8.2
        ...
        $ brew cask install netbeans-java-ee
        ```

* Homebrew

  * [Trouble Shooting](https://docs.brew.sh/Troubleshooting)
    * brew update
    * brew doctor
  * update gcc may take more than 1 hour
