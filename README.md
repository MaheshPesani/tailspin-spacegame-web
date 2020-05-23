For more details:
https://aka.ms/devops-build

Source: https://github.com/MicrosoftDocs/mslearn-tailspin-spacegame-web

git checkout master
git pull origin master
git checkout -b code-workflow

Push your branch to GitHub
git status
git add azure-pipelines.yml
git commit -m "Add the build configuration"
git push origin code-workflow