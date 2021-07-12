---
title: How I started with Git and Github
published: true
---

As far as I can remember it was the time of [Hacktoberfest-2019](https://hacktoberfest.digitalocean.com/) hosted by [amFOSS](https://amfoss.in/) when first time I had heard about Git & GitHub. We were supposed to create `Pull Requests` and they were monitoring who were creating their `PR` faster and top 10 were getting rewards. Not only by them even we can get official rewards like T-Shirt and cool stickers from Hacktoberfest for creating three Pull Requests. Well that's a preety fun way to start with Git,isn't it?

…do you really just want to contribute to your first open source project?

This one’s for you!

> It’s totally easy to get started with Git. If you’re a fast reader (and you don’t take a lot of time with sign up and installation), you can be up and running on GitHub about ten minutes from right now.
> 

If you go all the way through the article, you can practice cloning an existing repository, creating a branch, making changes, and creating a pull request. Along the way, you might also learn how to find your terminal, use terminal commands, and edit a markdown (.md) file!

This article will get you up and running with the basics. There’s a lot of stuff to learn if you want to use Git and GitHub like a pro, of course. You can go way beyond this introductory information! We’re going to leave the next-level stuff for another time, though.

Let’s get started!

## [](#header-2)What is Git? What’s GitHub?

> Git is the version control tech of choice for basically everybody right now, from developers to designers. GitHub is the social code-hosting platform that’s currently used more than any other. It’s a place where you can play and experiment. It’s a place where you can find (and play around with) the most incredible open-source information, emerging technologies, features, and designs. It’s a place to learn and it’s a place to get involved. You can keep code there for work or for school, and you can grab some sweet code that you want to explore further. You can even host websites for free directly from your repository! 
[If you want to know how to do that, check out this article!](https://towardsdatascience.com/how-to-create-a-free-github-pages-website-53743d7524e1)

There are a ton of ways to use Git and GitHub, but getting started with GitHub doesn’t have to be overwhelming. You don’t need to be some kind of master coder or anything. You can even do the most important things right on the GitHub website!

That being said, it’s a good idea to find your terminal and get just the tiniest bit comfortable with it. Terminal commands make things so much faster! I’ll definitely show you how to get started using the GitHub website. I’ll also show you some terminal commands that you might want to use to make your life just a little bit nicer.

> Any time you see a command in this article that includes these marks:`< >`, you want to delete those marks and replace what’s between them with your own information.
Let’s say you see something like `git add <filename>`. That means that you would type, for example, `git add hello_world.py` if you wanted to add a file named “hello_world.py” to your GitHub repository.

I’m going to give you a lot of explanation here, but these are all the terminal commands that you really need to know to get started:

```
git clone
git status
git add
git commit -m " "
git push
```

That’s it! Those are the big ones! If you have a handle of those, you’re good to go. You can start working on your projects immediately!

We’ll also talk about

```
git init
git branch
git merge
git checkout
```
You might be working with other people, or you might want to make changes and test them out before you really commit them. The commands above are what you need to get started with collaboration.

```
git help
```
is also seriously useful if you’re just starting out! We’ll discuss that too.

(If you’re on a Mac, you already have a terminal! You can search for it by clicking on the magnifying glass icon in the upper right-hand corner of your screen and searching for the word “terminal.” )

#### [](#header-3)Step 1: Sign up and installation!

Go to [GitHub](https://github.com/) and sign up for an account. You could just stop there and GitHub would work just fine. It’s a good idea, though, to [install Git](https://git-scm.com/downloads) if you haven’t already. You can absolutely get started without it, but if you want to work on your local computer, then you want to have Git installed. You can download it or [install it via your package manager instead](https://gist.github.com/derhuerst/1b15ff4652a867391f03).

Now go to your terminal and introduce yourself to Git! To set your username for *every repository* on your computer, type

```
git config --global user.name "<your_name_here>" 
```
replacing `"<your name here>"` with your own name in quotations. You can use any name or handle you want. If you want to set your name for just one repository, leave out the word “global.”

Now you can tell Git your email, and make sure it’s the same email you used when you signed up for GitHub

```
git config --global user.name "<your_name_here>"
```
It’s easy to keep your email private, and you can find those instructions in [this article](https://docs.github.com/en/github/setting-up-and-managing-your-github-user-account/managing-email-preferences/blocking-command-line-pushes-that-expose-your-personal-email-address). You only need to check two boxes in your GitHub account.

#### [](#header-3)Now you’re ready to start using Git on your computer!

To get started, you can create a new repository on the GitHub website or perform a `git init` to create a new repository from your project directory.

The repository consists of three ‘trees.’ First is the **working directory**, which holds the actual files. The second one is the **index** or the staging area. Then there’s the **head**, which points to the last commit you made.

#### [](#header-3)I’m already comfortable with the terminal (Option 1)

Here’s how you can get started right from the terminal:
```
git init 
```
If you want to initialize your project with all of the files in your project directory, run
```
git init .
```
to include everything.

Let’s say you have a folder for your project called “new_project.” You could head on over to that folder in your terminal window and add a local repository to it by running
```
cd new_project
git init
```

Now you have a new hidden directory called `.git` in your project directory. This is where Git stores what it needs so that it can track your project. Now you can add files to the staging area one by one with
```
git add <filename_one>
```
or run

```
git add .
```
to add all of your files to the staging area. You can commit these changes with the command

```
git commit -m "<add a commit message here>"
```

and if you’re happy with your changes, you can run
```
git push
```
to push your changes through. You can check whether or not you have changes to push through any time by running
```
git status
```
If you made some changes, you can update your files on at a time with
```
git add <filename>
```
or
```
git add --all
```
Then commit them with your commit message and push them through.

That’s it! You can now initialize a repository, commit files, commit changes, and push them through to the master branch.

If you’ve got this, just scroll down to “**Learning to work with others**” to move on to branching and collaboration!

#### [](#header-3)I don’t know what you just said (Option 2)

I’m going to assume that anyone who’s interested in option 2 is brand new to all of this and maybe has a folder full of files (or you plan to have one) that you want to put on GitHub and you just don’t know how to do that.

Let’s make that happen!

Say you want to create a new repository. (You probably do! That’s where your project will live. If you aren’t going to create a new repository, you probably want to clone an existing repository. We’ll talk about that next, but that’s how you grab someone else’s project and information that you need for your job or the course you’re taking.)

Your **repository** is where you’ll organize your project. You can keep folders, files, images, videos, spreadsheets, Jupyter notebooks, data sets, and anything else your project needs. Before you can work with Git, you have to initialize a repository for your project and set it up so that Git will manage it. You can do this right on the GitHub website.

It’s a smart idea to include a **README** file with information about your project. You can create one at the same time that you create your repository with the click of a checkbox.

* Go to the GitHub website, look in the upper right corner, and click the + sign and then click “New repository.”
* Name the repository, and add a quick description.
* Decide whether you want this to be a public or a private repository
* Click “Initialize this repository with a README” if you want to include the README file. (I definitely recommend doing this! It’s the first thing people are going to look at when they check out your repository. It’s also a great place to put information that you need to have in order to understand or run the project.)
<img src= "https://github.com/RanitPradhan/blog/blob/master/Images/blog1.jpg">
###### [](#header-6)Header 6

| head1        | head two          | three |
|:-------------|:------------------|:------|
| ok           | good swedish fish | nice  |
| out of stock | good and plenty   | nice  |
| ok           | good `oreos`      | hmm   |
| ok           | good `zoute` drop | yumm  |

### There's a horizontal rule below this.

* * *

### Here is an unordered list:

*   Item foo
*   Item bar
*   Item baz
*   Item zip

### And an ordered list:

1.  Item one
1.  Item two
1.  Item three
1.  Item four

### And a nested list:

- level 1 item
  - level 2 item
  - level 2 item
    - level 3 item
    - level 3 item
- level 1 item
  - level 2 item
  - level 2 item
  - level 2 item
- level 1 item
  - level 2 item
  - level 2 item
- level 1 item

### Small image

![](https://assets-cdn.github.com/images/icons/emoji/octocat.png)

### Large image

![](https://guides.github.com/activities/hello-world/branching.png)


### Definition lists can be used with HTML syntax.

<dl>
<dt>Name</dt>
<dd>Godzilla</dd>
<dt>Born</dt>
<dd>1952</dd>
<dt>Birthplace</dt>
<dd>Japan</dd>
<dt>Color</dt>
<dd>Green</dd>
</dl>

```
Long, single-line code blocks should not wrap. They should horizontally scroll if they are too long. This line should be long enough to demonstrate this.
```

```
The final element.
```
