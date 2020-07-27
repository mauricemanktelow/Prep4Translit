# Prep4Translit
## Description

The program imports a Microsoft word document (docx) and creates a new version which, by default, duplicates all Greek and Hebrew text in readiness for producing a transliteration using SIL's TECkit program. (It can be extended to other language sets - see below for more detail)

For example:    
*&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;This is the common verb היי in the Qal binyan*       
would become    
*&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;This is the common verb היי} היי} in the Qal binyan*

## Preparation
Before running the program, the original Word file to be processed should define a unique style which can be applied to the transliterated text. 

##### Recommendation to help with checking the inserted text
From practical experience with the progrma, due to the compxities of using space in mixed directional text, it has been found that on 0.5% of occasions the transliterated text is not correctly separated from the previous text by a space. The result of applying the transliteration therefore needs checking for correct insertion of spaces. The following recommendations help to make this a quick and simple process.  

It is recommended that the unique style to be added to the text for transliteration should be 1 or2 points larger than the original and coloured red. (It can subsequently be changed once checking is complete.)

The program provides an option to apply unique characters surrounding the transliterated text (these are called delimiters). It is recommended that characters such as {} be used. They can subsequently be easily removed using find/replace within Microsoft Word.

If, in use, the success rate is significantly less than that with any particular text please contact support by opening an [issue](https://github.com/mauricemanktelow/Prep4Translit/issues).
   
## Computer Requirements

This is a Windows (only) program which requires the .Net Framework version 4.5.2 or later, e.g. it will work with Windows 10

## Getting Started

As the program consists of a single exe file an installer has not been provided</br>
Download a copy of the program and put it in a folder on your computer and run the program in the normal way (by clicking on the file name).

Hopefully the program will be intuitive/self explanatory. For more detail download the documentation file.

##Methodology
To identify the words / phrases which need transliteration the program uses a range of unicode values. Four standard sets are provided:

* Arabic (U+0700-U+074F)
* Greek (U+0370-U+03FF  U+1F00-U+1FEE  U+0342-U+0345)
* Hebrew (U+0590-U+1FFE)
* Syriac (U+0700-U+074F)

These four are available via a drop down list. 

Users can specify their own unicode blocks by entering the values in the language block for transliterion. This can be either a set of single code points or a range as in the four standard sets above.

## Have a question or want to make a contribution

Please feel invited!

If you have a question, idea, or issue then please open an [issue](https://github.com/mauricemanktelow/Prep4Translit/issues) and I will get back to you as soon as possible
