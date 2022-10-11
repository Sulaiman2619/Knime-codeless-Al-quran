# Knime-codeless-Al-quran-Test 
##  Overview
  This project is about the Qur'an. To compare the translators with what percentage are the same by using Surat Al -Fatihah to compare. A total of 14 translators were used and Dr. Mustafa Khattab was used as a comparison. And it's the first project to try text mining using knime.

## Method
1.Import Excel file into knime using.
  * node Excel reader.

![Imgur](https://i.imgur.com/OaxnTe3.png)

### Result

![Imgur](https://i.imgur.com/IFnzA5a.png)

2.Bring the ayah of the translator together in 1 row for 1 person, total 14 people. using 
  * Node Row Fillter
  * Node GroupBy
  * Node Concatenate

![Imgur](https://i.imgur.com/qrTQIdZ.png)

### Result

![Imgur](https://i.imgur.com/au1hIJs.png)

3.Change data from String to Document using 
  * Node Strings To Document.

4.Select only the columns we want to use by using
  * Node Column Fillter

![Imgur](https://i.imgur.com/n4Ttv5A.png)

### Result

![Imgur](https://i.imgur.com/DB5IQRk.png)

5.Text Processing, remove extra words, remove unnecessary words, change to lowercase letters to make the writing the same, change verb to box 1, cut numbers with words, split words into individual words. as shown below:
  * Node Punctuation Erasure
  * Node stop Word Fillter
  * Node Case Converter
  * Node Snowball Stemmer
  * Node N Chars Fillter
  * Node Bag Of Words

![Imgur](https://i.imgur.com/BvVU2bp.png)

### Result

![Imgur](https://i.imgur.com/w2Kli1f.png)

6.Model Use TF and IDE to find word frequencies. by using
  * Node TF
  * Node IDF

7.TF and IDF are multiplied together for more accurate results. by using
  * Node Math Formula

![Imgur](https://i.imgur.com/1jjhGz1.png)

### Result

![Imgur](https://i.imgur.com/tLNFAup.png)

8.Combine the obtained values. by using
  * Node Document Vector
  
![Imgur](https://i.imgur.com/YzGfM6r.png)

### Result

![Imgur](https://i.imgur.com/GfqcB2u.png)

9.Select only the words that we want to use. and the people we will compare. by using
  * Node Column Fillter
  * Node Row Fillter
 
 ![Imgur](https://i.imgur.com/zcwNvh4.png)
 
 
 10.A selected and prepared comparator is taken to test for similarity. by using
  * Node Similarity Search
  
 ![Imgur](https://i.imgur.com/fi50efX.png)
 
### Result
 
 ![Imgur](https://i.imgur.com/JBiO1Ja.png)
