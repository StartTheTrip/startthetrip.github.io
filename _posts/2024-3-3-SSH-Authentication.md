---
layout: post
title: SSH Authentication
---

## Windows 10 ##
### Git SSH Authentication for Windows ###
To login to Git using command line on Windows 10.<br/>
<br/>
1. Open PowerShell and enter:<br/>
<br/>
ssh-keygen<br/>
<br/>
2. Follow the instructions to generate a key pair.<br/>
<br/>
If the key is a custom name open .ssh/config in a text editor, add:<br/>
<br/>
Host github.com<br/>
  IdentityFile ~/.ssh/KEYNAME_rsa<br/>
<br/>
3. In PowerShell enter:<br/>
<br/>
winget install --id GitHub.cli<br/>
<br/>
4. Close PowerShell<br/>
<br/>
5. Create an auth token at: <a href="https://github.com/settings/tokens/new">GitHub New Token</a><br/>
<br/>
6. Open PowerShell and enter:<br/>
gh auth login<br/>
github.com<br/>
ssh<br/>
Key location e.g. /.ssh/id_rsa<br/>
Enter auth token <br/>
<br/>
<br/><br><br>
Tag: Security, SSH

