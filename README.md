<h1>🔐 File Permissions in Linux </h1>


<h2>Description</h2>
The research team at my organization needs to update the file permissions for certain files and directories within the projects directory. I must examine and manage the permissions on the files in the /home/researcher2/projects directory for the researcher2 user. The researcher2 user is part of the research_team group.
The permissions do not currently reflect the level of authorization that should be given. I must check the permissions for all files in the directory, including any hidden files, to make sure that permissions align with the authorization that should be given. If they do not match, I must change the permissions.
Checking and updating these permissions will help keep the system secure.
<br />


<h2>Check file and directory details</h2>

 <b> The code lists all contents of the projects directory. I used the ls command with the -la option to display a detailed listing of the file contents that also returned hidden files. The output of my command indicates that there is one directory named drafts, one hidden file named .project_x.txt, and five other project files. The 10-character string in the first column represents the permissions set on each file or directory.</b> 
<p align="center">
<img src="https://imgur.com/IXaKZHV.png" height="700%" width="70%" alt="NV"/>
<img src="https://imgur.com/kXqM4bt.png" height="80%" width="80%" alt="RG"/>

<h2>Describing the permissions string </h2>

 <b>The 10-character string can be deconstructed to determine who is authorized to access the file and their specific permissions. The characters and what they represent are as follows:
- <b>1st character: This character is either a d or hyphen (-) and indicates the file type. If it’s a d, it’s a directory. If it’s a hyphen (-), it’s a regular file. </b>
- <b>2nd-4th characters: These characters indicate the read (r), write (w), and execute (x) permissions for the user. </b>
- <b>5th-7th characters: These characters indicate the read (r), write (w), and execute (x) permissions for the group. </b>
- <b>8th-10th characters: These characters indicate the read (r), write (w), and execute (x) permissions for other. This owner type consists of all other users on the system apart from the user and the group. </b>  

 <h2>Change file permissions</h2>

<b>The organization determined that other shouldn't have write access to any of their files. To comply with this, I referred to the file permissions that I previously returned. I determined project_k.txt must have the write access removed for other. </b>

- <b>The first two lines of the screenshot display the commands I entered, and the other lines display the output of the second command. The chmod command changes the permissions on files and directories. The first argument indicates what permissions should be changed, and the second argument specifies the file or directory.</b>
  
- <b>  In this example, I removed write permissions from other for the project_k.txt file. After this, I used ls -la to review the updates I made.</b>
<p align="center">
<img src="https://imgur.com/beqwlRU.png" height="80%" width="80%" alt="file perm"/>


<h2>Change file permissions on a hidden file</h2>

- <b>The research team at my organization recently archived project_x.txt. They do not want anyone to have write access to this project, but the user and group should have read access. 
</b>

- <b> I know .project_x.txt is a hidden file because it starts with a period (.). In this example, I removed write permissions from the user and group, and added read permissions to the group. I removed write permissions from the user with u-w. Then, I removed write permissions from the group with g-w, and added read permissions to the group with g+r.</b> 
<p align="center">
<img src="https://imgur.com/N1WTtk5.png" height="80%" width="80%" alt="remove"/>
<img src="https://imgur.com/8KQncmL.png" height="80%" width="80%" alt="add"/>
<img src="https://imgur.com/cDLfFoS.png" height="80%" width="80%" alt="display"/>

<h2>Change directory permissions</h2>

- <b>The research team at my organization recently archived project_x.txt. They do not want anyone to have write access to this project, but the user and group should have read access. 
</b>

- <b> I know .project_x.txt is a hidden file because it starts with a period (.). In this example, I removed write permissions from the user and group, and added read permissions to the group. I removed write permissions from the user with u-w. Then, I removed write permissions from the group with g-w, and added read permissions to the group with g+r.</b> 
<p align="center">
<img src="https://imgur.com/yfWVIkL.png" height="80%" width="80%" alt="remove"/>

<h2>Summary</h2>

 <b> I changed multiple permissions to match the level of authorization my organization wanted for files and directories in the projects directory. The first step in this was using ls -la to check the permissions for the directory. This informed my decisions in the following steps. I then used the chmod command multiple times to change the permissions on files and directories</b> 




