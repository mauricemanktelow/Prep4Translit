## Technical information

### Code
This Windows program was written in C# using Visual Studio 2015 Community Edition

### Methodology
After completing a number of checks that the parameters provided are valid the program then:

* Asks for the name of the file (docx) to be processed
* Asks for the name of the resulting processed file
* Checks the style to be applied is contained within the original document file
* Parses the initial document.xml file contained within the docx (zip) file to create its own xml tree
* Creates a linear list of text elements equation and relating back to the relevant text elements in the xml tree
* Uses a regular expression to identify words and phrases within the text elements which are candidates for transliteration
* For each candidate it inserts a duplicate of the associated xml element into the tree after having first added the defined delimiters
* Copies the original file and replaces the document.xml with the updated one
* Saves the file

### Limitation
Since the text is identified by a regular expression it will obviously only insert candidates for transliteration which it finds. The regular expression used has been developed by reverse engineering some existing documents and covers 99.5% of found cases. The difficulty lies in the number of possible permutations and combinations made possible within the bi-directional text with the use of inserted direction markers and direction over-writes within the xml tags.  
