# Developing and Deploying React App in Github Pages.
React is a propular library to develop user interfaces. Rich support for different libraries makes it a popular option among the developer community.

Let us see how to deploy a Personal Portfolio in Github pages. This is done for Windows machine. But with small modifications, this can be used for any operating system.

## In Github (https://github.com/) <br>
>Create a repository in Github. <br>
 Name this repository {your-user-name}.github.io
## In your computer
 > Download and Install NodeJS If you have not already(https://nodejs.org/en). <br> I suggest downloading LTS version.<br>
 > Verify If node is installed. Open Temrinal(or Command prompt)<br>
>```$node -v```
><br> This should show something like v20.0.0.
><br> In Terminal
><br> ```$npm install -g create-react-app```
<hr>

>Open Terminal, create a new React App.
><br>```$create-react-app "your-app-name"```
><br> ```$cd your-app-name```
><br> Set the Github repository as remote 
><br> ```$git commit -m "initial commit"```
><br> ```$git branch -M main```
><br> ```$git remote add origin https://github.com/your-user-name/your-username.github.io```
><br> ```$git push -u origin main```
><br>Install ```gh-pages``` as a dev dependency
><br> ```$npm install gh-pages --save-dev```

<hr>

>Let us configure package.json
> Add this in scripts property
><br>```"predeploy" : "npm run build",
> "deploy" : "gh-pages -d build",```
> <br>Add the following into properties
><br> ```"homepage":"https://{username}.github.io/{repo-name}"```
<br> It should look something like
```
  "name": "my-app",
  "version": "0.1.0",
  "homepage": "https://gitname.github.io/react-gh-pages",
  "private": true,
```
>```$git add .```
><br>```$git commit -m "setup gh-pages"```
><br>```$git push```
><br>Push the React app to the Github Repository
><br>```$ npm run deploy```


## In Github (https://github.com/) <br>
> Go to "Settings" in your respoitory
> Within Code and automation on the left pane, click on ```Pages```. 
><br>Source: Deploy from a Branch
><br>Branch: gh-pages
><br>Folder: /(root)

### Voila, You have set-up React application with Github Pages.
### Happy Programming