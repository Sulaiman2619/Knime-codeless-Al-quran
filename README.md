# Knime-codeless-Al-quran-Test 
##  Overview
  The project is a text mining project which uses Ayah Al-Qur'an Surah Al-Fatihah for text mining by taking the text that each translator translates to find the similarity. By using the process of text mining, in text mining we used the knime program in text mining which was the first project. which the benefits of this project It is able to do a search engine that will be able to search the meaning and find the meaning of other translators as well.

## Method
### Access Data
1. Extract data from Excel.
By using:
* Node Excel Reader

![Imgur](https://i.imgur.com/B5P3IWr.png)

#### Result

![Imgur](https://i.imgur.com/Fg4r2Rp.png)

### Tranform Data

![Imgur](https://i.imgur.com/3JLnuzC.png)

1.Remove unused data.
By using:
* Node Column Filter.

#### Result

![Imgur](https://i.imgur.com/5lgYJy6.png)

2.Convert data from column to row 
By using:
* Node Transpose

#### Result

![Imgur](https://i.imgur.com/miW0oaK.png)

3.Combine each column of text into a single column. And removes unused columns. 
By using:
* Node Column Combiner
* Node Column Fillter

#### Result

![Imgur](https://i.imgur.com/kkNLN2Y.png)

4.Create a new column in the table and combine it with the original table. 
By Using :
* Node Table Creator
* Node Column Appender

#### Result

![Imgur](https://i.imgur.com/MkUiUty.png)

![Imgur](https://i.imgur.com/6CKLher.png)

5.Remove Dashes from Text
By using:
* Node String Manipulation

#### Result

![Imgur](https://i.imgur.com/2QlYP2t.png)

### Text Processessing

![Imgur](https://i.imgur.com/9LcQiax.png)

1.Convert String to Document where Title will be Column tran_id and Text will be column surah. And then delete the columns that are not in use.
By using:
* Node Strings To Document
* Node Column Fillter

![Imgur](https://i.imgur.com/XUB2Gd1.png)

#### Result

![Imgur](https://i.imgur.com/a3ndYxi.png)

2.Remove special words such as , : _ ^ etc., change all letters to lowercase, remove unnecessary words. Frequently encountered words such as the,to,and etc.
By using:
* Node Punctuation Erasure
* Case Converter
* Stop Word Filter

#### Result

![Imgur](https://i.imgur.com/IC1a60A.png)


    
