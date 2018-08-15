# Trying out doxygen documentation on gh-pages

git checkout master

mkdir doc
cd doc
mkdir html
cd ../..

echo "doc/html/" >> .gitignore

git add .gitignore
git commit -m "Added html doc folder"
git push origin master

cd doc/html/
git clone yourRepository

cp the files of the repo in /html/
rm the folder

git checkout -b gh-pages
git branch -d master

git rm everything except .git

git commit -m "Removed everything"

cd ../..
doxygen -g doxygen.conf

set OUTPUT_DIRECTORY = ./doc/

git checkout master
doxygen doxygen.conf

cd doc/html/
git checkout gh-pages

git add *
git commit -m "Added html doc"
git push origine gh-pages
