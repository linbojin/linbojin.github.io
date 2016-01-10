Build blog with Hexo and MWeb
-------------------------------
My blog: https://linbojin.github.io/

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
1. Install [hexo-deployer-git](https://github.com/hexojs/hexo-deployer-git)

	```bash
	$ npm install hexo-deployer-git --save
	```
2. Edit `{blog}/_config.yml`

	```bash
	$ vim _config.yml
	
	# Deployment
	deploy:
	  type: git
	  repo: git@github.com:username/username.github.io.git
	  branch: master
	```
3. Deploy after you make any changes and go to your blog https://username.github.io

	```bash
	$ hexo deploy -g
	```
	
4. You can also test local: http://0.0.0.0:4000/
	
	```bash
	$ hexo server
	```

### Tips
1. Back up `source` folder and add **version control**: markdown source files will be inside `{blog}/source` and this folder will not be tracked by git. So I sync this important folder to cloud:

	```bash
	$ cp -r {blog}/source {Dropbox}/blog/source
	$ vim _config.yml # point source_dir to the new synced path  
		
	# Directory
	source_dir: {Dropbox}/blog/source
	```

2. Add README.md to repo: create README.md inside `{source}` folder and modify `{blog}/_config.yml`, so that **README.md** can introduce your repo on github like this one:

	```bash
	$ vim _config.yml
		
	# Directory
	skip_render: README.md
	```
	
### Congratulations, Enjoy your blog ^-^



---------------------------
Ref: [Hexo](https://hexo.io/docs/index.html), [MWeb for Octpress](http://zh.mweb.im/mweb-1.4-add-floder-octpress-support.html) 

