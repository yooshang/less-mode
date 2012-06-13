forked from myfreeweb/less-mode

不使用 css-mode, 使用 c-mode

.less文件保存后，会触发自动编译，自动替换路径中的 '/less/' => '/css/' 并加上 '.css' 后缀，
例如：

    lessc --no-color -x /less/*.less > /css/*.less.css

html还是直接引用 /css/*.less.css 文件

# less-mode #
Major Emacs mode for editing [Less](http://lesscss.org) files.
Inspired by myfreweb's [less-mode](https://github.com/myfreeweb/less-mode).

## Installation ##

    (require 'less-mode)
    (add-to-list 'auto-mode-alist '("\\.less$" . less-mode))

If you use [smart-compile](http://www.emacswiki.org/emacs/SmartCompile):

    (add-to-list 'smart-compile-alist '(less-mode . (less-compile)))

If you use [Flymake](http://www.emacswiki.org/emacs/FlyMake), it will work automatically.
