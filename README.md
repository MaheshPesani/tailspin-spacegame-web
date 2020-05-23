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

git checkout master
git pull origin master

Build and run the web application
dotnet build --configuration Release
dotnet run --configuration Release --no-build --project Tailspin.SpaceGame.Web

Create a feature branch
git checkout -b feature/home-page-text
git add Tailspin.SpaceGame.Web/Views/Home/Index.cshtml
git commit -m "Improve the text at the top of the home page"
git push origin feature/home-page-text