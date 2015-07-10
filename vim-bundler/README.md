**lean and mean Vim image made to support persistent and swappable plugins and workspaces.**

*How to start Vim with your plugins and ".vimrc" file:*

```
docker run -ti -v <***/bundle>:/bundle -v <***/.vimrc>:/.vimrc  -v <***/workspace>:/home/developer/workspace jare/vim-pathogen
```

*You can add plugins and ".vimrc" file into the container:*

```
docker run -ti --name my-vim -v <***/bundle>:/bundle  -v <***/.vimrc>:/.vimrc jare/vim-pathogen add-bundle
docker commit my-vim my/vim-pathogen
```

*How to edit a file:*

```
docker run -ti --rm -v <***/workspace>:/home/developer/workspace my/vim-pathogen ./mydoc
```
**But why???**  
*This image can help progressively add and test new plugins and setting with versioning.*