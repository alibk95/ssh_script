# Git switcher
## Simple way to handle multiple git repo's in one client.
I had really hard time dealing with two git repo's in my machine as I wanted to access and switch between my work Bitbucket git and personal gitHUb repo on one machine.

After googling around and trying multiple ways I was finally able to fix the issue thanks to [Matthew Morrissette](https://gist.github.com/yinzara/bbedc35798df0495a4fdd27857bca2c1) This is actually the recommended way of doing it on Linux but you might get several errors on the way and it would be too overwhelming for most of us. Specially when you are on Linux machine.
##### For this reason I tried to implement a simple shell script so each time you want to switch to the other repo you just need tcodeo run the script and enjoy it

### How it works
![flowchart](https://github.com/alibk95/ssh_script/blob/master/ssh_flowchart.png "Diagram")

##### preperation
- create two directories in .ssh dir, one 'personal' and the other one 'work'
- move both private and public keys (id_rsa & id_rsa.pub) to the directories
- check if the .ssh itself is empty of any keys left.
- All set! Hell Yeah!

Run the script anywhere you prefer. Don't forget to change the permissions beforehand.

`chmod +x ./main_script.sh`

`bash ./main_script`

to make it much more easier I put the alias of the command in .bashrc file. 

`nano ~/.bashrc`
and add the following line to the end of the .bashrc file
`# aliases`
`alias swgit="bash ~/Desktop/git_switcher"`

so next time I just need to type the swgit in the CL. 
