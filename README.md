In school, I was given the choice of learning emacs or Vim. I decided to choose Vim, because it comes pre-installed on most servers, which generally run linux.

I got a lot of practice using vim in school, but I would call it brute force practice. We never talked about best practices as it comes to Vim.

I found this great article about [how to practice VIM deliberately](https://medium.com/actualize-network/how-to-learn-vim-a-four-week-plan-cd8b376a9b85). The second tip (constructing your vimrc file from the ground up) interests me because it’s not wise in coding to input things you don’t know. You should know what every line does (so when something breaks, you can troubleshoot efficiently). Last year, I installed [Ultimate Vim](https://github.com/amix/vimrc) and decided to un-install it, and build from the ground up.

The aforementioned article leads you [here](https://dougblack.io/words/a-good-vimrc.html), but the Colors section does not take you step-by-step in the installation properly. I had to read [this](https://www.mkyong.com/linux/how-to-install-a-vim-color-scheme/) additionally to understand that I need to create a directory for colorschemes.

The step-by-step instructions on how to do add a colorscheme (in this case, badwolf):
* `mkdir .vim .vim/colors` [make the directory to hold your colorscheme file]
* `cd ~/.vim/colors/` [go into your directory that will hold the colorscheme file]
* `.vim badwolf.vim` [open up the badwolf file]
* copy and paste the raw file
* Save and quit

badwolf is now installed. I also added comments in my .vimrc for each line to remind my future self of what each line does, in case I want to change it up later. I spent an hour and a half doing all this.

I wanted to see if I could do all this from the CLI (preferable, because it’s faster), so [I asked](https://stackoverflow.com/questions/51989852/copy-paste-from-raw-file-on-web-into-vim). Here is the one line command from the CLI:
`wget bitbucket.org/sjl/badwolf/raw/tip/colors/badwolf.vim -O ~/.vim/colors/badwolf.vim`

(P.S. To try that one-line command, I wanted to delete the contents of the file, without deleting the file, so I could try the answers from stackoverflow, and I found it:
`> badwolf.vim`)
