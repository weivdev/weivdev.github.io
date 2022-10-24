---
layout: post
title:  "Github Website Page Usage Tutorial!"
date:   2022-10-24 00:06:56 +0100
categories: github
---
## How to Setup Github Page Website
This article is about:
- how to setup github page website for my personal tech blog here: https://weivdev.github.io
- how to post and release more articles
  
#### 😈 The first time you tried to set up:
- Step 1: create a new public repo under your github with your personal username `weivdev/weivdev.github.io`
- Step 2: clone this repo to your local and try to push out a hello world homepage
    ```
    $ git clone https://github.com/weivdev/weivdev.github.io.git
    $ cd weivdev.github.io
    $ echo "Hello World" > index.html

    $ git add --all
    $ git commit -m "Initial commit"
    $ git push -u origin master
    ```
- Step 3: setting up Jekyllrb
    ```
    # install / update ruby
    $ brew install chruby ruby-install xz
    $ ruby-install ruby
    $ echo "source $(brew --prefix)/opt/chruby/share/chruby/chruby.sh" >> ~/.zshrc 
    $ echo "source $(brew --prefix)/opt/chruby/share/chruby/auto.sh" >> ~/.zshrc 
    $ echo "chruby ruby-3.1.2" >> ~/.zshrc # run 'chruby' to see actual version
    $ ruby -v

    # install Jekyll
    $ gem install jekyll
    ```
- Step 4: install Bundler: https://bundler.io/
  - create `Gemfile` under project root with below content
    ```
    source 'https://rubygems.org'
    gem 'nokogiri'
    gem 'rack', '~> 2.2.4'
    gem 'rspec'
    ```
  - run below under project folder
    ```
    $ bundle install
    $ git add Gemfile Gemfile.lock
    ```
- Step 5: set up in your Github repo page: 
  - Settings -> Code and Automation -> Pages:
    - choose `Deploy from a branch`
    - choose `Branch -> master -> /docs -> save`
- Step 6: under your local repo root folder:
  - create subfolder `docs` and new `jekyll`
    ```
    $ cd docs
    $ jekyll new --skip-bundle .
    ```
  - modify the newly created Gemfile in the `docs` folder
    - comment out `# gem "jekyll", "~> 4.3.0"`
    - uncomment `gem "github-pages", "~> 227", group: :jekyll_plugins`
      - check https://pages.github.com/versions/ the Version of `github-pages` is where the 227 from
    - save the Gemfile


#### 🌏 Add and publish articles
- add your new article `2022-10-24-my-article-title.markdown` file under `/docs/_posts`
- reference on how to edit your `markdown` file:
  - https://jekyllrb.com/
  - https://github.com/jekyll/minima
  - https://github.com/jekyll/jekyll
- commit and push the changes
    ```
    $ git add .
    $ git commit -m 'Initial GitHub pages site with Jekyll'
    $ git push -u origin master
    ```

##  👋 Thank you for reading my article ! 
#### 💰 Buy Me a Cup of Milk Tea 🧋?
- Ethereum Name Service Domain: `colaa.eth`
- Mainnet addresses:
  - address to receive ETH: `0x2eD8Ab8Ec7066F45fC3Ff07Ef4053D5c7180367f`
  - address to receive DOGE: `DDCSXuM231A4WRH4thqDjxvCfBdyQHPSu6`
## 👋 Cheers !
