- [前置](#前置)
- [插件快捷键](#插件快捷键)
  - [easymotion/vim-easymotion](#easymotionvim-easymotion)
  - [justinmk/vim-dirvish](#justinmkvim-dirvish)
  - [junegunn/fzf](#junegunnfzf)
  - [asins/vim-dict](#asinsvim-dict)
  - [NERDTree](#nerdtree)
  - [Yggdroot/LeaderF](#yggdrootleaderf)
# 前置
快捷键说明
```
<S-…> Shift＋键  
<C-…> Control＋键  
<M-…> Alt＋键 或 meta＋键  
<A-…> 同 <M-…> 解释：ideavim用的这个方式  
<leader> 默认是`\`键
```
# 插件快捷键
## easymotion/vim-easymotion
可视化快速跳转
快捷键
```
      Default Mapping      | Details
      ---------------------|----------------------------------------------
      <Leader>f{char}      | Find {char} to the right. See f.
      <Leader>F{char}      | Find {char} to the left. See F.
      <Leader>t{char}      | Till before the {char} to the right. See t.
      <Leader>T{char}      | Till after the {char} to the left. See T.
      <Leader>w            | Beginning of word forward. See w.
      <Leader>W            | Beginning of WORD forward. See W.
      <Leader>b            | Beginning of word backward. See b.
      <Leader>B            | Beginning of WORD backward. See B.
      <Leader>e            | End of word forward. See e.
      <Leader>E            | End of WORD forward. See E.
      <Leader>ge           | End of word backward. See ge.
      <Leader>gE           | End of WORD backward. See gE.
      <Leader>j            | Line downward. See j.
      <Leader>k            | Line upward. See k.
      <Leader>n            | Jump to latest "/" or "?" forward. See n.
      <Leader>N            | Jump to latest "/" or "?" backward. See N.
      <Leader>s            | Find(Search) {char} forward and backward.
                           | See f and F.
```
具体可参考`:help easymotion.txt`
## justinmk/vim-dirvish
可视化文件浏览器
```
 Global
      <Plug>(dirvish_up)
      -               Opens the current file directory or the [count]th parent.

  Buffer-local (filetype=dirvish)
      g?              Shows this help.
      [count]R        Reloads the current directory. (:edit works too.)
                      Sets g:dirvish_mode to [count], if given.
                      Mnemonic: higher [count] => more files.
      <Plug>(dirvish_quit)
      gq              Quits and returns to the original file.
      <Plug>(dirvish_up)
      -               Opens the [count]th parent directory.
      <Plug>(dirvish_split_up)
                      Opens the [count]th parent in a new window.
      <Plug>(dirvish_vsplit_up)
                      Opens the [count]th parent in a new, vertical window.
      <2-LeftMouse>
      i
      <CR>            Opens file at cursor.
      {Visual}I
      {Visual}<CR>    Opens selected files.
      o               Opens file in a new window.
      {Visual}O       Opens each selected file in a new window.
      a               Opens file in a new, vertical window.
      {Visual}A       Opens each selected file in a new, vertical window.
      K               Shows file info. [count] shows directory size.
      {Visual}K       Shows info for selected files. [count] shows directory size.
      p               Previews file at cursor.
      CTRL-N          Previews the next file.
      CTRL-P          Previews the previous file.
       <Plug>(dirvish_arg)
      x               Adds/removes file to/from the local arglist.
      {Visual}x       Adds selected files to the local arglist.
      dax             Starts a new empty local arglist.
      .               Inserts ":! {path}" into the command-line.
      {Visual}.       Inserts ":Shdo  {}" into the command-line.
      [count].        Inserts ":Shdo! {}" into the command-line.
      ~               Opens your home directory.
      cd              Sets the local current-directory. :lcd
      [count]cd       Sets the global current-directory. :cd
```
具体可以查看`:help dirvish`
## junegunn/fzf
文件搜索工具
```
" Look for files under current directory
      :FZF

      " Look for files under your home directory
      :FZF ~

      " With fzf command-line options
      :FZF --reverse --info=inline /tmp

      " Bang version starts fzf in fullscreen mode
      :FZF!
```
具体可以查看`help fzf`
## asins/vim-dict
关键字补全
在输入模式下按<ctrl-x>_<ctrl-k>即可看到提示内容。
## NERDTree
树型文件浏览器
```
 Default
  Key      Description                                                  help-tag

  o........Open files, directories and bookmarks......................NERDTree-o
  go.......Open selected file, but leave cursor in the NERDTree......NERDTree-go
           Find selected bookmark directory in current NERDTree
  t........Open selected node/bookmark in a new tab...................NERDTree-t
  T........Same as 't' but keep the focus on the current tab..........NERDTree-T
  i........Open selected file in a split window.......................NERDTree-i
  gi.......Same as i, but leave the cursor on the NERDTree...........NERDTree-gi
  s........Open selected file in a new vsplit.........................NERDTree-s
  gs.......Same as s, but leave the cursor on the NERDTree...........NERDTree-gs
  <CR>.....User-definable custom open action.......................NERDTree-<CR>
  O........Recursively open the selected directory....................NERDTree-O
  x........Close the current nodes parent.............................NERDTree-x
  X........Recursively close all children of the current node.........NERDTree-X
  e........Edit the current directory.................................NERDTree-e

  double-click....same as NERDTree-o.
  middle-click....same as NERDTree-i for files, and NERDTree-e for directories.

  D........Delete the current bookmark ...............................NERDTree-D

  P........Jump to the root node......................................NERDTree-P
  p........Jump to current nodes parent...............................NERDTree-p
  K........Jump up inside directories at the current tree depth.......NERDTree-K
  J........Jump down inside directories at the current tree depth.....NERDTree-J
  <C-J>....Jump down to next sibling of the current directory.......NERDTree-C-J
  <C-K>....Jump up to previous sibling of the current directory.....NERDTree-C-K

  C........Change the tree root to the selected directory.............NERDTree-C
  u........Move the tree root up one directory........................NERDTree-u
  U........Same as 'u' except the old root node is left open..........NERDTree-U
  r........Recursively refresh the current directory..................NERDTree-r
  R........Recursively refresh the current root.......................NERDTree-R
  m........Display the NERDTree menu..................................NERDTree-m
  cd.......Change the CWD to the directory of the selected node......NERDTree-cd
  CD.......Change tree root to the CWD...............................NERDTree-CD

  I........Toggle whether hidden files displayed......................NERDTree-I
  f........Toggle whether the file filters are used...................NERDTree-f
  F........Toggle whether files are displayed.........................NERDTree-F
  B........Toggle whether the bookmark table is displayed.............NERDTree-B
  
  q........Close the NERDTree window..................................NERDTree-q
  A........Zoom (maximize/minimize) the NERDTree window...............NERDTree-A
  ?........Toggle the display of the quick help.......................NERDTree-?
  ```
  另外配置脚本里还自定义了快捷键：
  ```
  	noremap <space>nn :NERDTree<cr>
	noremap <space>no :NERDTreeFocus<cr>
	noremap <space>nm :NERDTreeMirror<cr>
	noremap <space>nt :NERDTreeToggle<cr>
```
  具体可查看`help NERDTree`
## Yggdroot/LeaderF
  NERDTree的超级替代者
  ```
        " CTRL+p 打开文件模糊匹配
		let g:Lf_ShortcutF = '<c-p>'

		" ALT+n 打开 buffer 模糊匹配
		let g:Lf_ShortcutB = '<m-n>'

		" CTRL+n 打开最近使用的文件 MRU，进行模糊匹配
		noremap <c-n> :LeaderfMru<cr>

		" ALT+p 打开函数列表，按 i 进入模糊匹配，ESC 退出
		noremap <m-p> :LeaderfFunction!<cr>

		" ALT+SHIFT+p 打开 tag 列表，i 进入模糊匹配，ESC退出
		noremap <m-P> :LeaderfBufTag!<cr>

		" ALT+n 打开 buffer 列表进行模糊匹配
		noremap <m-n> :LeaderfBuffer<cr>

		" ALT+m 全局 tags 模糊匹配
		noremap <m-m> :LeaderfTag<cr>
```