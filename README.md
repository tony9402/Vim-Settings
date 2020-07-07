# Vim-Settings

## 목표

종강을 한 기념으로 귀찮아서 설정하지 않았던 vim을 세팅해보려 한다.
vim에 플러그인을 깔면 작업효율이 더 좋아지므로 얼른 세팅을 해보자

## [Plugin Manager](https://github.com/junegunn/vim-plug)

예전엔 [Vundle](https://github.com/VundleVim/Vundle.vim)을 사용했지만 검색을 해보니 vim-plug가 더 끌려서 사용해보려고 한다.

## 플러그인

어떤 플러그인을 설치할지 몇일동안 검색을 하며 고민을 해보았다.(어떤 플러그인을 깔지 결정을 하면 까는데는 몇분도 안걸리지만 vim 환경 세팅을 잘 하고 싶어 이것저것 엄청 찾았다.

1.  [nanotech/jellybean.vim](https://github.com/nanotech/jellybeans.vim)
2.  [majutsushi/tagbar](https://github.com/majutsushi/tagbar)

    ctags을 깔아야 함 (brew install --HEAD universal-ctags/universal-ctags/universal-ctags)
3.  [scrooloose/nerdtree](https://github.com/preservim/nerdtree)

    단축키 설정을 추가로 함 

    E -> NERDTreeToggle
4.  [nathanaelkane/vim-indent-guides](https://github.com/nathanaelkane/vim-indent-guides)

    IndentGuidesToggle(단축키 설정 안함)
5.  [airblade/vim-gitgutter](https://github.com/airblade/vim-gitgutter)
6.  [tpope/vim-fugitive](https://github.com/tpope/vim-fugitive)
7.  [vim-airline/vim-airline](https://github.com/vim-airline/vim-airline/vim-airline)
8.  [vim-airline/vim-airline-themes](https://github.com/vim-airline/vim-airline-themes)
9.  [blueyed/vim-diminactive](https://github.com/blueyed/vim-diminactive)
10. [junegunn/vim-easy-align](https://github.com/junegunn/vim-easy-align)
11. [Valloric/YouCompleteMe](https://github.com/Valloric/YouCompleteMe)
12. [honza/vim-snippets](https://github.com/honza/vim-snippets)
13. [SirVer/ultisnips](https://github.com/ultisnips)
14. [terryma/vim-multiple-cursors](https://github.com/terryma/vim-multiple-cursors)

## Customermize Snippets

#### 현재 만든 Snippet

1. Main
2. SegmentTree Class
3. Euclid Functions

Snippet 변경 위치
```bash
/Users/$USER/.vim/plugged/vim-snippets/snippets/
```

#### Snippet 설정 방법
```vim
snippet ma
    include<bits/stdc++.h>
 
     #define all(x) (x).begin(),(x).end()
     using namespace std;
     typedef long long ll;
     typedef pair<int, int> pii;
     ll MOD = 1e9 + 7;
 
     int main(){
         ios::sync_with_stdio(false); cin.tie(0);
         ${0}
         return 0;
     }
```

## Customermize Theme

