## build ##             
sudo docker build -t evan/vim .        

## use ##           
#### Make an alias: ####
alias viedit='sudo docker run -ti --rm -v $(pwd):/home/developer/workspace evan/vim'         
Have fun!  viedit some.file
