---
title: Setting up a version controlled, static blog using Hakyll & Github
author: Vikas Menon
---
You can use Github for hosting a blog (1). 

The only compromise is:

(1) You won't have control over your account name. It will always be of the form: gitusername.github.io.
(2) You can only host static pages

These work as a reasonable compromises for me. If they work for you; you can read how I created this setup:

Steps to install:

      (a) Setup a github repository with the name username.github.io
      (b) Create index.html:
      	 echo "Hello Hakyll World!" > index.html 
	 	  git add index.html
	          git commit -am "Updating index.html"
		  git push
      (c) Visit username.github.io (vikasmenon.github.io in my case)

Voila! You have setup your own static blog!

You then have multiple options like Jekyll, Middleman and many more to make beautiful static websites that are easy to create and low maintainence. 

I chose Hakyll because I'm also learning Haskell and figured it would be useful learning experience. Here is the official Hakyll tutorial page (2)

Steps to setup:

      (a) cabal init sandbox #If you haven't used sanboxes before: Here is a good reference (3) 
      (b) cabal update
      (c) cabal install hakyll

Now that we have setup Hakyll. We will use it to create a template blog:

    (a) cabal build site.hs
    (b) ./dist/build/site/site build

Testing out your website:

	(a) ./dist/build/site/site watch
	(b) Visit: http://localhost:8000/

I simply modified the existing templates to create my website. I believe there is a lot more you can do in terms of customization. A good place to start is to learn from others (4)

References: 

(1) https://pages.github.com/
(2) http://jaspervdj.be/hakyll/tutorials.html
(3) http://coldwa.st/e/blog/2013-08-20-Cabal-sandbox.html
(4) http://jaspervdj.be/hakyll/examples.html

PS: I'll improve the markdown on this post in the next version and include guides/notes