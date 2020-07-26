# Prep4Translit
## Description

The program imports a Microsoft word document (docx) and creates a new version which, by default,duplicates all Greek and Hebrew text in readiness for producing a transliteration using SIL's TECkit program. (It can be extended to other language sets - see below for more detail)

For example:    
*&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;This is the common verb היי in the Qal binyan*       
would become    
*&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;This is the common verb היי} היי} in the Qal binyan*

## Preparation
Before running the program the original Word file to be processed should define a unique style which can be applied to the transliterated text. 

##### Recommendation to help with checking the inserted text
From practical application of the program it has been found that on 0.5% of occassions the transilterated text is not seperated form teh previous text by a space - therefore the result of applying the transliteration needs checking for correct insertion os spaces. The following recommendations help to mak this a quick and simply process.  

The unique style to be added to the text for transileration should be 1 or2 points larger than the original and coloured red. It can subsequently be changed once checking is complete.

The program provides an option to apply unique characters surrounding the transilerated text (these are called delimiters). It is recommended that characters such as {} be used. They can subsequently be easily removed using find/replace within Microsoft Word.
   
## Computer Requirements

This is a Windows (only) program which requires the .Net Framework version 4.5.2 or later, e.g. it will work with Windows 10

## Getting Started

As the program consistes of a single exe file an installer has not been provided</br>
Download a copy of the program and put it in a folder on your computer and run the program in the normal way (by clicking on the file name).

Hopefully the program will be intutitve / self explanatory. For more detail download the documentation file.

##Methodology
To identify the words / phrases which need transileration the program uses a regular espression. The one used has been developed by experimentation with a range of texts. It has been found to work on 99.5% of occasions - with minor spacing issues with the remainig 0.5%. If the success rate is significanlty les than that with any particualr text please contact support by opening an [issue](https://github.com/mauricemanktelow/Prep4Translit/issues).

## Working with character sets other than Hebrew or Greek

The original brief for the program was to work with Hebrew and Greek. This can easily be extended to other character sets by ammending the regular experession used in the conversion.

The default regular expression for Hebrew and Greek is:
(\([\u0370-\u03FF\u1F00-\u1FFF\u0342-\u0345\u2019\u0590-\u05FF\u202A\u202C\u200E\u200F]+\))*([\u0370-\u03FF\u1F00-\u1FFF\u0342-\u0345\u2019\u0590-\u05FF\u202A\u202C\u200E\u200F]+)([\s\u202A\u202C\u200E\u200F\u2026\u2025\u002E{2,3}\u002D\u2011\u2012\u2013\u2014]*([\u0370-\u03FF\u1F00-\u1FFF\u0342-\u0345\u2019\u0590-\u05FF]+[\u202A\u202C\u200E\u200F]*)+)+(\s*\([\u0370-\u03FF\u1F00-\u1FFF\u0342-\u0345\u2019\u0590-\u05FF\u002D\u2011\u2012\u2013\u2014]+\))*

In the above experession the Greek block is defined as \u0370-\u03FF\u1F00-\u1FFF and the Hebrew block is \u0590-\u05FF. To include another language block alloccurrences of these blocks will require either replacing adding to with the required additonal language block.

For example to work with the Syriac code block \u0700—\u074F insted of Greek and Hebrew the regular expresion would need modifying as follows:

(\([\u0700—\u074F\u0342-\u0345\u2019\u202A\u202C\u200E\u200F]+\))*([\u0700—\u074F\u0342-\u0345\u2019\u202A\u202C\u200E\u200F]+)([\s\u202A\u202C\u200E\u200F\u2026\u2025\u002E{2,3}\u002D\u2011\u2012\u2013\u2014]*([\u0700—\u074F\u0342-\u0345\u2019]+[\u202A\u202C\u200E\u200F]*)+)+(\s*\([\u0700—\u074F\u0342-\u0345\u2019\u002D\u2011\u2012\u2013\u2014]+\))*


## Have a question or want to make a contribution

Please feel invited!

If you have a question, idea, or issue then please open an [issue](https://github.com/mauricemanktelow/Prep4Translit/issues) and I will get back to you as soon as possible
