# Hosting Resume on a static site.  
> Step by step guide on how to host and format a resume on GitHub pages using Jekyll themes, based on general principles of current [Technical Writing](https://www.amazon.ca/Modern-Technical-Writing-Introduction-Documentation-ebook/dp/B01A2QL9SS). The **EXPLANATION** part below some of the steps touch up on the underlying principles as to why that step is important.

## Prerequisites:  

The reader should have the following before starting the steps mentioned below:  
- A resume formatted in **Markdown**. 
- A working internet connection.  
- Any prefered web browser  

## INSTRUCTIONS:  
  
### STEP 1: Creating a GitHub account
> If you already have an account set up on GitHub, Sign in and then proceed to Step 2.
1. Go to [GitHub homepage](https://github.com/). 
2. Click on **Sign up** located top right of the screen.
3. Enter your email in the prompted space and press **Continue**.
4. Create a _strong_ password in the prompted space and press continue.
    > A strong password contains at least 15 characters OR at least 8 characters including a number and a lowercase letter.  
5. Enter the desired username and press **Continue**.  
    > It might take a few tries to land on a username that is available.
6. Enter **y** if you want to recieve email updates, otherwise entre **n** and press continue.  
7. Solve the puzzle for verification . 
8. Click on **Create Account**.  
9. Verify your account by entering the code sent to the email enterd above.
10. Follow along the basic information questions.
11. Choose the account that suits you best.
    > For this guide the free version was selected.  

#### EXPLANATION:
Using a distributed version control (such as GitHub in this case) for documentation is important for many reasons:     
- For starters it is preferred by the developers.  
- Having the documentation and the product in the same repository is convenient.
- It promotes contribution from the developers and others. 

### STEP 2: Creating your Repository  
> A repository is the collection of all your project's files and cointains informational history about all the changes made to the project. You can read more about GitHub Repository [here](https://docs.github.com/en/repositories/creating-and-managing-repositories/about-repositories).  
1. Click on the **'+'** at the top right of the screen and from the dropdown menu choose **New Repository**.  
2. Enter the desired name for the repository.  
3. (Optional) Enter a short discription of the project for which the repository will be used for.
4. Select the **Public** option.
5. (Recommended) Add a README.md . 
6. Click on **Create repository** at the bottom of the page.  

#### EXPLANATION:  
In this step its important to actually touch up on what a repository is so that the user with no prior experience can know about what they are doing instead of just blindly follow steps. Which is exactly what the starter for "Basic functional document" is according to Andrew Etter.

### STEP 3: Adding files to the repository
Now that the repository is created the next steps involves uploading the required documents to it.
> Make sure the resume is saved as ***index.md*** in order for it to be hosted.  

1. Click on **Add File** and select **Upload files** from the dropdown menu.  
2. From here there are two ways in which documents can be uploaded. It does not make much difference as to which method is used.
    - Drag and drop your resume file in the dedicated box or,
    - Clicking the **choose your file** option and then go to the path where the resume is saved on your system.
3. Add a commit message. ( A short description as to what changes were made) 
4. Click on **Commit changes**.

#### EXPLANATION:  
Using your resume as a markdown file is also another principle of technical writing where using a lightweight markup language is considered as a far better option than using something like MS Word for example. These markup languages are more human readable than HTML or XML and easily customizable.

### STEP 4: Creating a configuration file for Jekyll  
>Jekyll is a static site generator that uses simple markup languages and creates complete website based on themes of your choice. _GitHub pages_ that we are going to be using to host our resume is based on Jekyll. More information about GitHub Pages and Jekyll can be found [here](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/about-github-pages-and-jekyll#about-jekyll).

In order for the static website to work we need a **__config.yml_** file in the root directory of where the _index.md_ is located. To add this file follow the steps:
1. Click on **Add File** and select **Create file** from the dropdown menu.  
2. Name the file __config.yml_. (For the site to work it is important that the file name should be exactly the same)
3. Now in the text box add the following code:  

    ```
    remote_theme: pages-themes/midnight@v0.2.0 # any other theme could be chosen in place of 'midnight@v0.2.0'.
    plugins:
    - jekyll-remote-theme # add this line to the plugins list if you already have one

    title: [WELCOME] # Or any other title you want.
 
    ``` 
4. Add a commit message like before and click **Commit changes**.  

#### EXPLANATION:  
Styling is another important factor to consider while documentation. Words are italicized for emphasis and bold for the user interface buttons etc. also the code chunk is monospaced for better distinction which ultimately leads to a better user understanding. 

### STEP 5: Setting up GitHub Pages
GitHub pages are GitHub's standard site generator which it uses to host websites. More about GitHub pages are really well explained in this [video](https://youtu.be/2MsN8gpT6jY).  
1. Click on **Settings** option from the top option bar.
2. Select **Pages** from the list of options on the left side of the screen. 
3. Under the **Branch** heading in the **Build and deployment** section, click on **None** and select **main** from the dropdown menu.
4. Click on **Save**.
> It takes up to 10 minutes for GitHub to get the site up and running. You might need to refresh the page. 

#### EXPLANATION:
Linking a video or other resources help in creating _topic_ in your steps. Single sourcing is a method in which the documents are divided into smaller categories known as 'topics' which are independent of one another. This makes it easier for user to understand individual pieces better also it makes it easier to update the document if one part changes.

### STEP 6: Going to the website:
Once GitHub is done with generating the website a link to the website appears at the top of the same page. You can click on **Visit site** to go to the page or open a tab in the web broweser and add the following link:  
_https://user_name.github.io/repository_name/_  
        
- Replace the _user_name_ with your GitHub username and _repository_name_ with the name of the repository that contains your resume and the config file.

## Visual Representstion
This is how the resume looks on simple markdown without any hosting on a website.
![Resume without hosting](https://github.com/Its-Adi-Kashyap/kashyap1.github.io/blob/main/src/Markdown_resume.gif?raw=true)  

This is what it looks after hosting it using GitHub pages and adding a theme using Jekyll.
![Resume with hosting](https://github.com/Its-Adi-Kashyap/kashyap1.github.io/blob/main/src/website_resume.gif?raw=true)

## MORE RESOURCES:  
- A Step by step markdown tutorial [here](https://www.markdowntutorial.com/).  
- Resource for basic principles of technical writing  [Modern Technical Writing by Andrew Etter](https://www.amazon.ca/Modern-Technical-Writing-Introduction-Documentation-ebook/dp/B01A2QL9SS)
- In-depth instructions about GitHub and it's various functionalities [here](https://docs.github.com/en/get-started/quickstart/hello-world).

## AUTHORS AND ACKNOWLEDGEMENT:
These instructions were written by Aditya Kashyap.
A huge shoutout to Said Mahmud for the guidance and instructions.  
Jekyll theme used in this setup: By [mattgraham](https://twitter.com/mattgraham)

## FAQ:

##### Question 1: Why is hosting the documentation on a website better than just having it locally on the device?
> Answer: The biggest advantage of having the documentation on a website, static or dynamic, is that its easy to update and distribute. Now instead of having different versions of the same files, users can just have the most upto date document. Any change made to the document automaticaly reaches the user. 

##### Question 2: Why does it says 404 not found when I try  to go to the    website ?  
        
>Answer: One of the reason could be because GitHub is not yet finished with building the website. Please wait for a while and then refresh the page. 
