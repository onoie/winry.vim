# VimPluginNote
メモ

## Tips

bashからvim commandを実行する
```
vim +":source ~/.vim/dein/repos/github.com/onoie/winry.vim/plugin/winry.vim " +:q
```

reload .vimrc
```
:source %
```

load vim script
```
:source ~/.vim/dein/repos/github.com/onoie/winry.vim/plugin/winry.vim
```

全選択  
`ggv<shift+g>`
ディレクトリ作成  
`:!mkdir -p %:h`


## Todo
[x] HelloWorld
[x] ToggleFunc
[x] pythonを実行
[ ] bashを実行


### 構文
コメント`'コメント`

### テンプレートからPluginを作成
[LayoutPlugin](https://github.com/mopp/layoutplugin.vim)
dein.toml
```vim
call dein#add('mopp/layoutplugin.vim')
```
`:LayoutPlugin winry.vim`

#### 各フォルダの用途
* /plugin
  vim立ち上げ時に読み込むvim script
* /autoload
  呼び出された時に初めて読み込む(dllっぽい動き?
pluginフォルダのスクリプト数は極力減らして
autoloadでメインの処理を書いたほうがいいらしい

### Vim scriptの型
```
型	例
数値	let foo = 1
文字列	let foo = "bar"
関数リファレンス	let Foo = function("Bar")
リスト(List)	let foo = ["foo", "bar"]
辞書(Dictionary)	let foo = {"bar": "bar"}
浮動小数点数	let foo = 3.14
```
### Vim scriptの関数
```
function Foo()
  echo "foo"
endfunction
```
`:call Foo()`




