# create-mac-ssh
Generate an SSH Key Pair Mac

Password for all

password that you have setup

Remove the file id_rsa
rm ~/.ssh/id_rsa

1. Regenerate the SSH Key Pair:

ssh-keygen -t rsa -b 2048 -C "tarun.appnox1@gmail.com"

2. Check for Existing SSH Key Pairs:

ls -l ~/.ssh/

3. Use a Different File Path:

ssh-keygen -t rsa -b 2048 -C "tarun.appnox1@gmail.com" -f ~/.ssh/id_rsa

4. Start the SSH agent by running the following command:

eval "$(ssh-agent -s)"

5. Then add your SSH private key to the SSH agent:

ssh-add ~/.ssh/id_rsa

6: Copy the SSH Public Key
pbcopy < ~/.ssh/id_rsa.pub

ssh-rsa AAAAB3NzaC1yc2EA111111AAADAQABAAABAQDDubOrU6jR2HN3EZ1JLAq4Cy1VEgr1aopKutTsYhVtsP90DAco/QaoFFyCkB3Tn0U8qgk5SmOyIjbd+rKOr4DA+6C/LOBIHs9iDM+TE/PxySN/NcZqGDCSVWrmvH6Jz7PFGqybvQK+01giO3C0kMxHe6jBk/sa3Xm8M5FMiY1DFtSJ/mZQDw115WGSTxRcIUHSavVLgSp91nl3d2T4FU7krfZeXx9PDM2/SESsRE87IbVPMeskx59wutK5Fm1DxP3pzApABnGh6WbE34IVF8yz15d9s8L+evihOUHi9Wahg9fTZJlqIuXUQZACmySq3Oz/A+muo7JI6vU7IKFy2iZb tarun.appnox1@gmail.com


7. Add SSH Key to Bitbucket
Log in to your Bitbucket account.
Click on your avatar in the bottom left corner and select Bitbucket settings.
In the left sidebar, click on SSH keys under Security.
Click on Add key.
In the Label field, enter a label for your SSH key (e.g., "MacBook Pro").
In the Key field, paste the SSH public key you copied earlier.
Click Add key.

8: Test the SSH Connection

ssh -T git@bitbucket.org

9: Test the SSH Connection

ssh -i ~/.ssh/id_rsa git@bitbucket.org
