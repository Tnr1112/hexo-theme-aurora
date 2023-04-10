`hexo init *nombreProyecto*`
cd nombreProyecto
git clone https://github.com/Tnr1112/hexo-theme-aurora themes/aurora
Cambiar el `theme: aurora` y el `permalink: /post/:title.html`
Agregar el archivo `_config.aurora.yml` con `cp themes/aurora/_config.yml _config.aurora.yml`

Ejemplo `_config.aurora.yml`
```yml
#! ---------------------------------------------------------------
#! Aurora Theme for Hexo
#! ---------------------------------------------------------------
#! Designed & Coded By TriDiamond
#! ---------------------------------------------------------------

#! ---------------------------------------------------------------
#! Site Configs
#！ @docs https://aurora.tridiamond.tech/guide/configuration.html
#! ---------------------------------------------------------------
site:
  subtitle: Tnr1112
  author: Tnr1112
  nick: 
  description: Soy un pentester por hobbie, estudiante de Ingeniería en Sistemas y programador. <br>Amante de romper cosas :)
  link: 'https://github.com/Tnr1112'
  language: es
  multi_language: true
  logo: /images/MistyCara.jpg
  avatar: /images/auroraLogo.png
  beian:
    number: ''
    link: ''
  police_beian:
    number: ''
    link: ''

#! ---------------------------------------------------------------
#! Authors Configs
#！ @docs https://aurora.tridiamond.tech/guide/authors.html
#! ---------------------------------------------------------------
authors:
  Tnr1112:
    name: Tnr1112
    avatar: /images/MistyCara.jpg
    link: https://github.com/Tnr1112
    description: Soy un pentester por hobbie, estudiante de Ingeniería en Sistemas y programador. <br>Amante de romper cosas :)
    socials:
      github: https://github.com/Tnr1112

#! ---------------------------------------------------------------
#! Menu Configs
#！ @docs https://aurora.tridiamond.tech/guide/menu.html
#! ---------------------------------------------------------------
menu:
  About: true
  Tags: true
  Archives: true

#! ---------------------------------------------------------------
#! Theme Config
#! @docs https://aurora.tridiamond.tech/guide/theme.html
#! ---------------------------------------------------------------
theme:
  dark_mode: true
  profile_shape: rounded # support `circle`, `diamond`, `rounded`
  feature: true
  gradient:
    color_1: '#24c6dc'
    color_2: '#5433ff'
    color_3: '#ff0099'

#! ---------------------------------------------------------------
#! Social Configs
#! @docs https://aurora.tridiamond.tech/guide/social.html
#! ---------------------------------------------------------------
socials:
  github: https://github.com/Tnr1112
  customs:
  ##! Example:
  ##! --- Using SVG
#  bilibili:
#    icon: http://localhost:4000/svg/bilibili.svg
#    link: https://live.bilibili.com/22619211

  ##! --- Using IconFont
  # baidu:
  #   icon: iconfont icon-baidu
  #   link: https://live.bilibili.com/22619211

  ##! --- Using FontAwesome
  # book:
  #   icon: far fa-address-book
  #   link: https://live.bilibili.com/22619211

#! ---------------------------------------------------------------
#! Site Meta Configs
#! @docs https://aurora.tridiamond.tech/guide/theme.html
#! ---------------------------------------------------------------
site_meta:
  cdn: cn
  favicon:
  description: ''
  keywords: ''
  author: ''

#! ---------------------------------------------------------------
#! Plugins
#! @docs https://aurora.tridiamond.tech/guide/plugins.html
#! ---------------------------------------------------------------

# For local development only!
gitalk:
  enable: true
  autoExpand: true
  clientID: ''
  clientSecret: ''
  repo: ''
  owner: 'Tnr1112'
  admin: ['Tnr1112']
  id: uid
  language: en
  distractionFreeMode: true
  recentComment: true
  proxy: ''

# Valine comment plugin (recommended!)
# see https://valine.js.org/quickstart.html
valine:
  enable: true
  app_id: ''
  app_key: ''
  avatar: ''
  placeholder: Leave your thoughts behind~
  visitor: true
  lang: en
  avatarForce: false
  meta: ['nick', 'mail']
  requiredFields: []
  admin: 'Tnr1112'
  recentComment: true

# Enable Busuanzi statistic plugin
# see http://ibruce.info/2015/04/04/busuanzi/
busuanzi:
  enable: true

copy_protection:
  enable: true
  author:
    cn: 作者
    en: Author
  link:
    cn: 本文来自于
    en: Article is from
  license:
    cn: 博客内容遵循 署名-非商业性使用-相同方式共享 4.0 国际 (CC BY-NC-SA 4.0) 协议
    en: This content is shared under the CC BY-NC-SA 4.0 protocol (Non-Commercial)

#! ---------------------------------------------------------------
#! Enable Aurora Bot Dia
#! @docs https://aurora.tridiamond.tech/guide/site-meta.html#custom-meta
#! ---------------------------------------------------------------
aurora_bot:
  enable: false
  locale: en
  bot_type: dia
  tips:

#! ---------------------------------------------------------------
#! Injections
#! @docs https://aurora.tridiamond.tech/guide/site-meta.html#custom-meta
#! ---------------------------------------------------------------
injects:
  scripts:
  css:
    - <link rel="stylesheet" href="static/css/ownStyle.css">
```

Para inicializarlo: `hexo clean & hexo g & hexo server`

Para agregar imágenes: `source/images`

Para deployar:
Agregar en _config.yml
```
deploy:
  type: git
  repo: https://github.com/Tnr1112/tnr1112.github.io
  branch: main
```
Para deployar el hexo: `hexo clean && hexo deploy`
