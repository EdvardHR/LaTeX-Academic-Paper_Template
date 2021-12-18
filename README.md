# LaTeX Template for Academic Papers 

LaTeX template created to manage academic papers or reports of any size with ease. Supports English (British) and Norwegian (Bokmål).

The template has one clean and one prefilled example-text version. 
The prefilled version is suggested for new users.

The template is created with the use of part-seperation in mind, and thus optimal for handeling large projects. 


When first initiating a new project using this template, go through the "paramteres.sty"-file to make the primary changes like langeuage (brit or nor), title , reference style (ieee or apa) etc.

All authors are put into the authors.txt-file as shown by placeholders. 

I personally will advice all users to make the habit to give all _files_ a name with _non-capital_ letters, while keeping all folders with a first _captial_ letter. This is to make it easier to navigate the nested folder structure. 

The reason of the nested folder structure is to maintain ease when navigating when file is getting large. This way of managing and structuring the project makes it wasy if parts are to be restructrued, moved or removed in/from the main "main.txt" that's outside any folder. 

I also suggest each folder to have a "main.txt" of its own where the _input{}_-comamnd can be used to order the folder's files as wanted.

Example (structrue):

Folders with files:

-SectionFolder0
- file0
- file1
- file2
- main.txt



-SectionFolder1
- file0
- file1
- file2
- main.txt



-main.txt

Then the content of  _main.txt_s:
main.txt:
1. \input{.\SectionFolder0\main.txt}\pagebreak (add _\pagebreak_ to start next "input" on a new page)
2. \input{.\SectionFolder1\main.txt}

SectionFolder0\main.txt:

1. \input{file0}
2. \input{file1}
3. \input{file2}

SectionFolder1\main.txt:
1. \input{file0}\pagebreak
2. \input{file1}
3. \input{file2}


This way, it is easy to change the order of the different files or section, as each section is a layer of its own.
This also imporves the workability when cooparating on a project as one easly can exlude the section one works with to avoid any issues from others.

This also imporves troubleshooting abilities as it is easier to controll each segment on its own. 
