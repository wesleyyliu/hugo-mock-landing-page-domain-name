# hugo-mock-landing-page
The GitHub Actions workflow defined in the gh-pages-deployment.yaml file automates the process of building and deploying a Hugo website to GitHub Pages.
1. Trigger: The workflow is triggered on a push to the main branch.
2. Job Definition: A job named deploy runs on an ubuntu-22.04 environment.
3. Checkout Source Repository:
The workflow uses the actions/checkout action to check out the source code of the repository.
It fetches submodules and the full history of the repository.
4. Initialize Hugo Environment:
The peaceiris/actions-hugo action is used to set up the Hugo environment.
It specifies the Hugo version (0.144.1) and enables the extended version.
5. Compile Hugo Static Files:
The hugo command is executed to build the static files for the website.
The flags used are -D (include draft content), --gc (garbage collect), and --minify (minify the output).
6. Publish to GitHub Pages:
The peaceiris/actions-gh-pages action is used to publish the compiled static files to the gh-pages branch.
It uses the GitHub token for authentication and sets the user details for the commit.
7. Custom Domain (Optional):
There is a commented-out section for specifying a custom domain if needed.