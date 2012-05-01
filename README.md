## My Custom Sublime conf

This is my very personal conf. I'm still building this so there's a lot missing.

I'll add the bundles/packages when I have time.

### Make your life easier

```sh
➜  ~  ln -s Library/Application\ Support/Sublime\ Text\ 2/Packages sublime
```

### Install

I put the stuff in the User folder in the Packages folder of Sublime so there's 0 risk of losing my conf when I upgrade Sublime

```sh
cd ~/sublime
mv User User.backup # so you don't lose your previous chances
git clone git@github.com:midu/sublime-conf.git User
```

Or something like that.

### What does it do

#### Theme

![](http://i.pb.lc/0f0q380K0E2M1Z220x1G/Screen%20shot%202012-04-30%20at%2011.50.08%20AM.png)

Uses the [Railscasts theme](http://railscasts.com/about), wich means you'll need the [Bitstream Vera Sans Mono](http://ftp.gnome.org/pub/GNOME/sources/ttf-bitstream-vera/1.10/) font installed on your system.

I also set a big ass `23 points` font size because I have a big screen and I like to see my text.

### Bundles

#### [SublimeLinter](https://github.com/Kronuz/SublimeLinter)

![](http://i.pb.lc/0S3D1C1w0X3S1A2S3a33/Screen%20shot%202012-05-01%20at%2012.01.33%20PM.png)

_Lints and adds inline hightlights of errors in a bunch of languages._

##### Install:

```sh
cd ~/sublime
git clone https://github.com/Kronuz/SublimeLinter
```

You also need `jshint` in the $PATH.

```sh
npm install jshint
```

If you don't have node, do this first:

```sh
brew install node # installs node
curl http://npmjs.org/install.sh | sh # installs npm
```

Then add in your shellrc file:

```sh
NODE_PATH=$NODE_PATH:/usr/local/lib/node_modules # or whatever path node gives you when you run brew install node
```

And you'll need to add the output of `npm bin` to your $PATH

##### Customizations

- [changed the theme](https://github.com/midu/sublime-conf/commit/b28b79a8e5f317dff2a075fcfcdf002060caea8c#diff-2) so the outline is "invisible"
- on save, errors show in the popup

