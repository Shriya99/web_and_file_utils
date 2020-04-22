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
#### Methods Description:
* `urlstat_with_dirpath(directory_path)`
This method takes path of directories having .url files (Internet Shortcut files) as argument and creates a `res.txt` file containing the up/down status list of all the websites in the working directory.
 *Note: While entering path prefix a 'r'. For eg. r'C:\Users\yourname\dirname' should be given as argument*
 
 * `urlstat_with_file(filepath)
 This method takes path of the file containing the list of URLs to be checked. It creates a `res.txt` file containing the up/down status list of all the websites in the working directory.
*Note: While entering path prefix a 'r'. For eg. r'C:\Users\yourname\dirname' should be given as argument*
  
