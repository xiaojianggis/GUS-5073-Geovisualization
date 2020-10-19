## Lecture 10. Host and publish your map online

This week we are going to talk about using Github and publish your webpage online. We have already created interactive choropleth map using localhost, but our webpage is not publicly accessible yet. After this week, we will be able to publish it through github and every other people can see your geoviz.

## Github and Git
GitHub is website that provides hosting for software development version control using Git. Git is a free and open source distributed version control system designed to handle everything from small to very large projects with speed and efficiency. GitHub is not only a code sharing and social networking site for developers. It is also a web hosting site.  Below I have outlined how to host spatial data and a web application from GitHub.  This workflow is perfect for small applications. 

## Github pages
For this exercise, we will use Github to create a simple webpage repository. In this repository, we have the HTML, CSS, and JS required for our webpage. A feature of Github is the ability to create a homepage using something called Github pages.

To use Github pages to host a static page, you have to name your repository very specifically.The following steps detail creating a repository and setting up the initial settings.

Working with Github is easy, there are two main ways you can work with Github, via command line, or with a desktop GUI. The instructions below will show you how to get started on the command line.

## 1. Sign up a Github account
Sign up for a Github account on the Github site in which you can host projects and maintain repositories. ([Link](https://github.com/join?source=header-home))

## 2. Create, join, or fork repositories in your Github account
Repositories are project locations in Github. A repository is the most basic element of GitHub. A repository contains all of the project files (including documentation), and stores each file's revision history. Repositories can have multiple collaborators and can be either public or private. You can create copies of repositories that other people have created by ‘forking’ it from their account to yours. Repositories can have parallel versions called branches. The main branch is called the ‘master’ branch. Branches are used when you want to make try changes, but don’t want to change or break a working existing version of the code.

On the Github site, let’s create a repository. Repositories can be used for many projects, allowing you to collaborate, share, and modify scripts, programs, and websites. Project repositories can be named just about anything, and you should pick something relevant to your project. For example, if you are creating a repository to host your web geoviz, name it something like "geoviz" and use it for your project code and files.

## 3. Login and create a repository
Click on the Repositories tab on your main profile page. On your Github profile page, click on the Repositories tab.

i. In the upper right corner, select ‘New’. Create a new repository.

ii. In the Create a new repository window, set up your repository.
Name the repository ‘username.github.io’, and replace username with your Github username. Give the repository a description, make it public, and initialize it with a README. Don’t worry about the license at this point.

iii. Click Create.
You now have an empty repository set up in which you can add files and set up a project.

Let’s get Git setup so we can interact with it via command line on our local machine to create, edit, and manage files.

## 4. Check if Git is installed on your Machine
Moving back to our local machine, we need to get git and Github setup so we can work with it.

**If you are using Mac**: Using Terminal, we are going to check for Git, and if it is not found, we will download and install necessary files.

**If you are using Windows**: Git does not work easily from the Windows command prompt. To easily use command line to interact with Github, you need to install Github for desktop where you can use Git Bash. This is a command line interface that allows you to run commands to create repositories, rectify file differences, and push commits.

[Download Github Desktop](https://desktop.github.com/)

Once downloaded, proceed below, but instead of using Terminal, you use Git Bash.

#### i. Open Terminal/Git Bash
#### ii. Check git installation by entering the following command
`git –-version`
if you have Git installed, you will see the version. If you get an error, or you don’t see the version, you need to install Git. Install Git from the downloads page on the main Git project homepage.

https://git-scm.com/

Download Git for your machine. A wizard will lead you through the installation. You can select the defaults for installation. You might need to restart your machine after installation to get it to take effect.


## 5. Link your local webpage dictory with your github repository
Initiate your git, by typing `git init`
type in `git remote add origin <your reposity name, such as https://github.com/boehnert/webpage.git>`. For example, I create a repository with name of `choroplethlead`, then I just need to type `git remote add origin https://github.com/xiaojianggis/choroplethlead.git`. This command will link your directory on your local machine with the GitHub repository.  You will see this command on GitHub under how to push an existing repository from the command line.

## 6. Create a branch for your repository
Branch is just like a virtual environment. We can create a seperate environment and do experiment inside it. Now you need to create a branch called `gh-pages` from GitHub and switch to this branch. Type in `git checkout -b gh-pages`. This command with switch to the gh-pages branch in the repository.

## 7. Commit everything in your folder to your repository
Now just commit everything in the folder to your repository by typing in `git add .`, then type in `git commit -m 'This is my initial commit'`

## 8. Push your project up to the branch on the Github repository
Push your project up to the branch gh-pages by typing in `git push origin gh-pages`

## 9. Open your webpage on Web browser
Now your project is up on GitHub. In a web browser log into your GitHub account and view the project in the gh-pages branch. You can also view the web site using your http://<GitHub handle>.github.io/repository name. My final website can be viewed at https://xiaojianggis.github.io/choroplethlead/


## Homework
1. Finish the tutorial and create a interactive and dynamic geoviz. 
2. Using a the field of "num_bll_5p", different color scheme, and different scale of legend
3. Upload your `.html` file to the Canvas. 

**Reference**: 
https://gis.ucar.edu/github-web-hosting



In this tutorial, we are going to publish our developed geoviz on Github. In previous tutorial, I assume you all have installed the Github desktop and Git bash environment successfully on your computer. 
**For Mac**, type in `git --version` in your terminal and see if your get the git installed
**For Windows**, open your `Git` bash, and type in `git --version`. 

If we have the github account registered and `git` bash configured successfully, let get started and publish our geoviz online. 

**All the folowing commands will be run in Git Bash, NOT Anaconda**


### 1. Create a repository
i. Click on the Repositories tab on your main profile page.
On your Github profile page, click on the Repositories tab.

ii. In the upper right corner, select ‘New’.
Create a new repository.

iii. In the Create a new repository window, set up your repository.
You name your repository as "geoviz" or other names you like. Give the repository a description, make it public. **Don't initialize it with a README.**

iv. Click Create.
You now have an empty repository set up in which you can add files and set up a project.

i. Click on the Repositories tab on your main profile page.
On your Github profile page, click on the Repositories tab.

### 2. Create a Directory for Github Projects on your Local Machine
Next we want to setup a Github folder on your computer that can contain local copies of our Github project directories. The easiest way to edit and change code is to work on it on your own machine. You can then sync the repository folders with the Github servers so others can see and use your code modifications, and you can pull changes others have made.

First, create a github directory on your machine. We are going to set up a github folder within the Documents folder of our local profile (documents/github) using Terminal and some basic command line to complete the task.

##### i. Open Terminal, change your current location to your Documents directory.
Use cd to change directories on your machine to the location you want to store documents.
```
cd you_dicrectory
```
**Note**: You can use `pwd` to find out your present working directory

##### ii. Create a new directory called ‘geovisualization’
Make a new folder that will hold our github projects.
```
mkdir geovisualization
```
This creates an empty folder called `geovisualization` in your folder. We will use this for storing local copies of our github repositories and as working space when we edit and modify your code and documents.

##### iii. Change the working directory to your new `geovisualization` directory
```
cd geovisualization
```
The ‘geovisualization’ folder is now your working directory and commands we run will be happening in this directory. We will work locally on our Github repositories in this space.

### 3. Clone an existing repo to your local computer
I prepare a repository on my github account, you can first use my code for this tutorial, but in your homework, you need to use your developed code. 

```
git clone https://github.com/xiaojianggis/geoviz.git
```
Then you will have a folder of `geoviz` in your directory. We are going to upload it to github. 

-------------------------------------------
**In your homewok, you need to start from here, forget about git clone**

If you want to upload your own web page to Github, you don't need to git clone anything, just `cd` to your folder of the code. **MAKE SURE** your html file is named as `index.html`, or you will not see your webpage.


### 4. Synchronize with your github repository
change your directory to the new created folder of `geoviz`. **In your homework, you need to change your directory to your code of the website**
```
cd geoviz
```
Then initiate your folder, 
```
git init
```

Alright, let start to Synchronize our local folder with Github repository, 
```
git remote add origin https://github.com/xiaojianggis/geoviztest.git
```
You need to replace the last paramter by the link of your repository. 

**Note**: if you get error of "fatal: remote origin already exists." Type the following statement to solve it,
```
git remote -v
git remote rm origin
git remote add origin https://github.com/xiaojianggis/geoviztest.git

```


### 5. Check out with a branch
Now you need to create a branch called gh-pages from GitHub and switch to this branch. Type in,
```
git checkout -b gh-pages
```
This command with switch to the gh-pages branch in the repository.

### 6. Add and commit your files to your repository
Now just commit everything in the folder to your repository by typing in 
```
git add .
git commit -m 'my initial commit, just a memo'
```

### 7. Finally push your project up to the branch gh-pages by typing in  
```
git push origin gh-pages 
```

### 8. Now your project is up on GitHub.  
In a web browser log into your GitHub account and view the project in the gh-pages branch.  You can also view the web site using your http://<GitHub handle>.github.io/repository name.  My final website can be viewed at https://xiaojianggis.github.io/geoviz/

Make sure you replace the `xiaojianggis` by your own user name, and `geoviztest` by your own repository name. 



## Reference:
MIT DUSP Geoviz, https://github.com/civic-data-design-lab/16_11.S947/blob/master/week1/Part1_IntroGitAndGithub.ipynb
Web hosting on Github, https://gis.ucar.edu/github-web-hosting
