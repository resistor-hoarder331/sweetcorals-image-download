# sweetcorals-image-download
A small how to guide on downloading a sweet corals image datatset from hugging face 

I used a git bash terminal, because it made life easier for me, and it gave me the actual image files, and not pointers.

Before you begin, have a hugging face account and you may need an access token (more on that later!).


Here is the step by step guide:

1. Login to Aqua
2. cd into the folder you'd like to store the images
3. In the terminal:
   1. mkdir -p ~/bin
   2. cd ~/bin
   3. wget https://github.com/git-lfs/git-lfs/releases/download/v3.5.1/git-lfs-linux-amd64-v3.5.1.tar.gz <break></break>
      <break>tar -xvzf git-lfs-linux-amd64-v3.5.1.tar.gz </break>
      You should see: git-lfs-linux-amd64-v3.5.1.tar.gz    100%[====================================================================>]   4.74M  21.7MB/s    in 0.2s (or something similar) <break>
   6. mv git-lfs-3.5.1/git-lfs ~/bin/
   7. rm -rf git-lfs-3.5.1 git-lfs-linux-amd64-v3.5.1.tar.gz
   8. echo 'export PATH="$HOME/bin:$PATH"' >> ~/.bashr
   9. source ~/.bashrc
   10. git lfs version
       You should see something like this: git-lfs/3.5.1 (GitHub; linux amd64; go 1.x)
   12. git lfs install --skip-repo
       git clone https://huggingface.co/datasets/wildflow/sweet-corals
       cd sweet-corals/_indonesia_tabuhan_p1_20250210/images

You should now have the images wherever you stored them!
   

