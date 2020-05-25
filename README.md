[![Build Status](https://maheshpesani.visualstudio.com/Space%20Game%20-%20web%20-%20Pipeline/_apis/build/status/MaheshPesani.tailspin-spacegame-web?branchName=master)](https://maheshpesani.visualstudio.com/Space%20Game%20-%20web%20-%20Pipeline/_build/latest?definitionId=18&branchName=master)

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

Synchronize any changes to the master branch
git checkout master
git pull origin master
git checkout feature/home-page-text
git merge master

git checkout -b bugfix/home-page-typo

Tests:
dotnet build --configuration Release
dotnet test --configuration Release --no-build
dotnet test Tailspin.SpaceGame.Web.Tests --configuration Release --no-build --logger trx
