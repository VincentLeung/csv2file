# csv2file

This script converts the content of a CSV file into a folder structure with TXT files as their content ready to use in Kirby.

# Example Input/Output

**CSV file input:**

`field1; field2; field3; field4`

**Output directories and files:**
```
output
  |__ field2
        |__ article.txt
```

The content of article.txt will result in:
```
Date: field1
----
Title: field2
----
Teaser: field3
----
Text: field4
----
```

# Installation

1. Clone or download this repo
2. run `npm install` in your csv2file directory

# Usage

run `node index.js <csvFile> [comma separated header]`

If no "comma separated header" is supplied, the script will use the 4 default headers: Date,Title,Teaser,Text
The supplied headers don't neccessarily have to match the amount of fields in your CSV file.

# Usage Example

run `node index.js sample.csv date-published, headline, teaser-text, body-content`

or using the default values:

run `node index.js sample.csv`

