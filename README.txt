Template Use Instructions (updated March 2008):

1) Open the master.tex file in your editor of choice and compile it the way it is (set the output profile in TeXnicCenter to "LaTeX => PDF" so that you get a PDF).  In some editors, you may have to compile it more than once for all the figure, table and bibliography references to be formed properly (TeXnicCenter will give you lots of warnings until it works out all of the references).

2) The output is a thesis/dissertation that is in the format that BYU wants the final version to be.  In many editors, compiling the document and viewing it are two separate operations, so if you compile it and the PDF file does not show up, find the button for viewing it.  You can also open the master.pdf file that is created in the same directory as the master.tex file.  If you do that, make sure you close it before trying to compile again, since the computer needs to write over it and it will not compile if the file is already open.

3) Dave Johansen compiled this template on the EE Unix/Linux boxes, the CS Linux boxes, and his own machine (MikTeX with Windows XP) and he included the .sty sheets needed for it to compile in all those settings. Ideally, you would get rid of them and have all those packages in your install of LaTeX and you'd keep them up to date, but they are there so that it can compile right out of the box for everyone. The files that would probably be installed on most LaTeX installations but are included here for completeness are chngpage.sty, keyval.tex, xkeyval.sty, and xkeyval.tex.

Other Little Tips (updated March 2008):

1) You will need to set all of the name properties or you can make them use defaults (big ugly text that says it is missing) by using the option usedefaultnames.

2) The copyrightyear will just set itself to the current year, but you can change that if you want.

3) You can turn off any part of the BYU header using the commands in the \byustylesetup{} on line 32 through 40.

4) LaTeX's \includeonly feature works here. Consult your favorite LaTeX resource for more information.

5) If you are using TeXnicCenter, make sure you create a project with master.tex as the main file.  This allows easy navigation through the entire document and through your references (helps avoid the warnings when you misspell a citation).

SUCCESS IN OBTAINING DEPARTMENT AND COLLEGE APPROVAL

1) Compile master.tex with line 6 of master.tex is uncommented and line 10 commented. This produces a "one-sided version" that, in PDF form is the official version of your thesis/dissertation. 

2) Print the file created in step 1) using one-sided printing. Submit the one-sided-printed version to the department for approval.

3) If you or your advisor desire a printed/bound version, you can bind the one-sided version. Alternatively, to save cost, create a version intended for 2-sided printing and print it two-sided. To do this, compile master.tex with line 6 of master.tex commented and line 10 uncommented. 


Printing Tips:

1) When you print your PDF make sure that "Page Scaling" is set to "None". The default value is "Fit to Printer Margins" and this will cause everything to be not quite the right size.

2) Also, check to make sure that your document is the right size (8.5" x 11"). It has been discovered that several LaTeX installations default to generating a document that is on A4 paper and this will cause your margins to be off throughout your document when you print. To fix this follow these steps (with MikTeX):
	2a) Go to the "dvipdfm\config" folder in your MikTeX installation ("C:\texmf" by default) and edit the "config" file in a text editor
	2b) Change "p a4" to "p letter"

	2c) Go to the "dvips\config" folder in your MikTeX installation ("C:\texmf" by default) and edit the "config.ps" file in a text editor
	2d) Make sure that "letterSize" is the first entry in the list of paper sizes by changing the order from

        @ A4size 594.99bp 841.99bp
       	@+ ! %%DocumentPaperSizes: a4
        @+ %%PaperSize: A4

        @ letterSize 8.5in 11in
        @+ ! %%DocumentPaperSizes: Letter

	to

	@ letterSize 8.5in 11in
        @+ ! %%DocumentPaperSizes: Letter

        @ A4size 594.99bp 841.99bp
        @+ ! %%DocumentPaperSizes: a4
        @+ %%PaperSize: A4
	