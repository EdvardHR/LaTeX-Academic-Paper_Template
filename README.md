# LaTeX Template for Academic Papers 

LaTeX template created to manage academic papers or reports of any size with ease. Supports English (British) and Norwegian (Bokmål).

The template has one clean and one prefilled example-text version. 
The prefilled version is suggested for new users.

The template is created with the use of part-separation in mind, and thus optimal for handling large projects. 


When first initiating a new project using this template, go through the "paramteres.sty"-file to make the primary changes like language (brit or nor), title , reference style (ieee or apa) etc.
If using clean-branch, the relevant line in "\Front\title page" must be commented back in again when/if inserting a picture/figure.

All authors are put into the authors.txt-file as shown by placeholders. 

I personally will advice all users to make the habit to give all _files_ a name with _non-capital_ letters, while keeping all folders with a first _captial_ letter. This is to make it easier to navigate the nested folder structure. 

The reason of the nested folder structure is to maintain ease when navigating when file is getting large. This way of managing and structuring the project makes it easy if parts are to be restructured, moved or removed in/from the main "main.txt" that's outside any folder. 

I also suggest each folder to have a "main.txt" of its own where the _input{}command can be used to order the folder's files as wanted.

Example (structure):

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
1. \input{\SectionFolder0/main.txt}\pagebreak (add _\pagebreak_ to start next "input" on a new page)
2. \input{\SectionFolder1/main.txt}

SectionFolder0/main.txt:

1. \input{file0}
2. \input{file1}
3. \input{file2}

SectionFolder1\main.txt:
1. \input{file0}\pagebreak
2. \input{file1}
3. \input{file2}


This way, it is easy to change the order of the different files or sections, as each section is a layer of its own.
This also improves the workability when cooperating on a project as one easily can exclude the section one works with to avoid any issues from others.

This also improves troubleshooting abilities as it is easier to control each segment on its own. 
