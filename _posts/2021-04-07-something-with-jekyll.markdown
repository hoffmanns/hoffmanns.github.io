# Something with jekyll
After reading the hackernews post [Don't End The Week With Nothing](https://training.kalzumeus.com/newsletters/archive/do-not-end-the-week-with-nothing), I had the itch to start with "something", but did not really know where to start, so I eventually forgot about it. 

Some weeks later, I was having a conversation with my brother-in-law about how to set up an simple static website. He asked me for help how on how to publish a simple HTML website for his art (mainly music and drawings) and which technology or platform could be used, I decided to find out by myself. Since I have been working as a backend webdeveloper for some time, I don't want him to use Wordpress (ughh). The first thing that came to my mind is github pages. Being a webdeveloper, some love for using git for the content comes naturally, so lets try this for myself.

## The good ol' ruby/brew rabbit hole

So here I am, fallen into the rabbit hole of updating ruby (2.3 -> 2.7) on my old private dev macbook (2.4+ needed to build a jekyll site), which naturally leads to update rvm first. Of course, RVM needs a brew update first (but only after rvm tries to install ruby 2.7 for 30 minutes). Brew update does not like some "taps", I must have installed some years ago, that need some untapping. Alright, update is still not working (gcc cannot be found ..). Maybe Mac command line tools need to be installed as well (as I have updated MacOS some month ago, my Xcode ceased to function), so lets download that. Ok, maybe that was the problem in the first place, now ruby 2.7 seems to be installing. Have been installing iTerm as well, as I have some time on my hand while waiting for the installation/compilation. I have the feeling that this could have been done a bit more efficient.

## jekyll

Now, finally lets dig into jekyll. This was easy.
Just typing 

```bash
gem install bundler jekyll
jekyll new . --force
```

and tweaking [some stuff](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/creating-a-github-pages-site-with-jekyll#creating-your-site) in the `Gemfile`, followed by a `bundle update` did the trick. I pushed everything to the github repo that contained my github page and my jekyll site was already served. Using jekyll will not be my recommandation for a non techie (esp. for a windows user, since jekyll is not supported on windows too well) but using yekyll on github pages is quite impressive, but I def. need to find out what yekyll really does (for my own purposes), and if github pages is suited for publishing simple HTML alongside with some media assets (not too sure about this one..)