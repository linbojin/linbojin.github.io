---
---

# linbojin.github.io
My Blog: https://linbojin.github.io/

## Build your blog by Hexo and MWeb

### Requirements
* [Github account](https://github.com/): blog deployed by GitHub Pages
* [Hexo](https://hexo.io/): blog framework to generate static blog files
* [MWeb](http://www.mweb.im/): Markdown writing tool

### Setup Github
1. Create a new repository named username.github.io
2. https://username.github.io will be your personal blog address

### Setup Hexo
Make sure you have installed node.js and git.

```
$ npm install -g hexo-cli
$ hexo init blog    
$ cd blog
$ hexo new "my first blog"
```

### Setup MWeb
1. Install MWeb in App Store
2. Lauch MWeb and go into `External Mode` (Command + E)
3. Add new external source: `{blog}/source`, and choose `Media Save Path` as `Absolute` 
4. Enjoy writing

### Deploy Blog
Install [hexo-deployer-git](https://github.com/hexojs/hexo-deployer-git)

```
$ npm install hexo-deployer-git --save
```

Edit `{blog}/_config.yml`

```
$ vim _config.yml

# Deployment
deploy:
	type: git
	repo: git@github.com:username/username.github.io.git
	branch: master
```
Deploy after you make any changes

```
$ hexo deploy -g
```

Go to your blog: https://username.github.io

### Tips
Your markdown source files will be inside `{blog}/source` and this folder will not be tracked by git. You'd better to sync this important folder to cloud:

```
$ cp -r {blog}/source {Dropbox}/blog/source
$ vim _config.yml # point source_dir to the new synced path  

  # Directory
    source_dir: {Dropbox}/blog/source
```

### Congratulations, Enjoy Your blog ^-^



---------------------------
Ref: [Hexo](https://hexo.io/docs/index.html), [MWeb for Octpress](http://zh.mweb.im/mweb-1.4-add-floder-octpress-support.html) 

