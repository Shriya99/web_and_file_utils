# web_and_file_utils - Package Description
This package contains simple web and file utilities in Python.It currently includes -
* Getting up/down status of a list of websites as a mail/text document from
  1. text file containing URLs list
  2. path of directories containing .url files (Internet Shortcut files) i.e. directories having bookmarked sites or favourite sites from        browsers
* Getting list of paths of all files of a particular extension from multiple directories in a text file(for easy access to their paths       during development and other purposes)

## Installation
Package can be installed as :
`pip install web_and_file_utils`

## Modules and Usages
Modules present in the package are : `getstat`, `mailstat`, `getdictstat` and `filepack`

### `getstat` module
#### Import as : `from web_and_file_utils import getstat`
#### Methods Description:
* `urlstat_with_dirpath(directory_path)`
This method takes path of directories having .url files (Internet Shortcut files) as argument and creates a `res.txt` file containing the up/down status list of all the websites in the working directory.
 *Note: While entering path prefix a 'r'. For eg. r'C:\Users\yourname\dirname' should be given as argument*
 
 * `urlstat_with_file(filepath)
 This method takes path of the file containing the list of URLs to be checked as argument. It creates a `res.txt` file containing the up/down status list of all the websites in the working directory.(Protocol should be present in the URLs in the file i.e. http, https etc should be mentioned)
*Note: While entering path prefix a 'r'. For eg. r'C:\Users\yourname\dirname' should be given as argument*

#### How to Call A Method : `getstat.urlstat_with_dirpath(directory_path)`

### `mailstat` module
#### Import as : `from web_and_file_utils import getstat`
#### Methods Description:
* `urlstatmail_with_dirpath(directory_path,fromadd,toadd,pswd,smtphost)`
This method takes path of directories having .url files (Internet Shortcut files),sender's mail id, recipient's mail id,sender's mail password and smtp server address as arguments and automatically mail a `res.txt` file containing the up/down status list of all the websites in the working directory.

 *Note: While entering path prefix a 'r'. For eg. r'C:\Users\yourname\dirname' should be given as argument*
 
**Disclaimer : In order to use this method with automatic mail function using your mail id,your id and password needs to be provided as arguments and you need to enable access to less-secure apps from your mail id.It uses the smtplib module. Make sure to use this method for personal use only and compulsorily delete all arguments containing data before sharing the script with anyone.In case of any privacy breach,creator of this package will not be responsible whatsoever.**

**Use the `getstat` module if you don't want the automatic mailing functionality**
 
 * `urlstatmail_with_file(filepath,fromadd,toadd,pswd,smtphost)
 This method takes path of the file containing the list of URLs to be checked,sender's mail id, recipient's mail id,sender's mail password and smtp server address as arguments. It automatically mails a `res.txt` file containing the up/down status list of all the websites in the working directory.(Protocol should be present in the URLs in the file i.e. http, https etc should be mentioned)
*Note: While entering path prefix a 'r'. For eg. r'C:\Users\yourname\dirname' should be given as argument*

**Disclaimer : In order to use this method with automatic mail function using your mail id,your id and password needs to be provided as arguments and you need to enable access to less-secure apps from your mail id.It uses the smtplib module. Make sure to use this method for personal use only and compulsorily delete all arguments containing data before sharing the script with anyone.In case of any privacy breach,creator of this package will not be responsible whatsoever.**

**Use the `getstat` module if you don't want the automatic mailing functionality**

#### How to Call A Method : `mailstat.urlstatmail_with_dirpath(directory_path,fromadd,toadd,pswd,smtphost)`



