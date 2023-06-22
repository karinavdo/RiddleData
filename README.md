# RiddleData
## Dataset from the Riddle of Literary Quality Project

**Authors:** Maciej Eder, Joris van Zundert, Karina van Dalen-Oskam, Saskia Lensink<br/>
**License:** [GPL-3](https://opensource.org/licenses/GPL-3.0)

This dataset contains the data of a reader survey about fiction in Dutch, a description of the novels the readers rated, and the results of stylistic measurements of the novels. 

There is also an [R-package](https://github.com/karinavdo/LitRiddleData) which contains these data and some convenience functions to explain, combine, analyze, and visualize these data, as well as some examples of how the data could be accessed and processed.

If you use the data from this repository in your academic publications, please consider citing it as follows: 

Eder, M., Van Zundert, J., Lensink, S., and Van Dalen-Oskam, K. (2023). RiddleData: Dataset from the Riddle of Literary Quality Project. (1.0.0). GitHub. <https://github.com/karinavdo/RiddleData>

If you prefer citing a publication, please either of these:

Maciej Eder, Lensink, S., Van Zundert, J.J., and Van Dalen-Oskam, K.H. (2022). “Replicating The Riddle of Literary Quality: The LitRiddle Package for R.” In _Digital Humanities 2022 Conference Abstracts_, 636–637. Tokyo: The University of Tokyo / DH2022 Local Organizing Committee. https://dh2022.dhii.asia/abstracts/163.

Karina van Dalen-Oskam (2023). _The Riddle of Literary Quality: A Computational Approach._ Amsterdam University Press.

## The Data

### books.csv
The 'books' dataset contains information on several details of the 401 different books used in the survey. The following is a list with the different column names and an explanation of the information they contain:

1.	**short.title** \
    A short name containing the author's name and (a part of) the title;
2.	**author** \
    Last name and first name of the author;
3.	**title** \
    Full title of the book;
4.	**title.english** \
    Full title of the book in English;
5.	**genre** \
    Genre of the book. There are four different genres:
    a) Fiction; b) Romantic; c) Suspense; d) Other;
6.	**book.id** \
    Unique number to identify each book;
7.	**riddle.code** \
    More complete list of genres of the books. Contains 13 categories:
    1. "301-302 (VERTAALDE) LITERAIRE ROMAN"
    2. "301-302 (VERTAALDE) LITERAIRE ROMAN Verhalenbundel*"
    3. "305 LITERAIRE THRILLER"
    4. "331 DETECTIVE"
    5. "332 THRILLER"
    6. "Andere*"
    7. "Humoristisch-Romantisch*"
    8. "Non-fictie*"
    9. "Non-fictie* [en meer dan 1 essay, KvDO]"
    10. "Non-fictie* [en te oud, en meerdere essays, KvDO]"  
    11. "Romantisch*"
    12. "Verhalenbundel*"
    13. "Young Adult* " 
8.	**riddle.code.english** \
    Translation of code in column 7 in English:
    1. "301 Literary novel / 302 translated literary novel"
    2. "301 Literary novel / 302 translated literary novel, short stories"
    3. "305 Literary thriller"
    4. "331 Detective"
    5. "332 Thriller"
    6. "Humoristic-romantic"
    7. "Non-fiction"
    8. "Non-fiction (and more than one essay, KvDO)"
    9. "Non-fiction (and too old, and collection of essays, KvDO)"
    10. "Other"
    11. "Romantic"
    12. "Short stories"
    13. "Young Adult"
9.	**translated** \
    'yes' if the book has been translated, 'no' if not;
10.	**gender.author** \
    The gender of the author: Female, Male, Unknown/Multiple;
11.	**origin.author** \
    The country of origin of the author. Note that short country codes have been used instead of the full country names;
12.	**original.language** \
    The original language of the book. Note that short language codes have been used, instead of the full language names;
13.	**inclusion.criterion** \
    In what category a book has been placed, either a) bestseller; b) boekenweekgeschenk; c) library; or d) literair juweeltje;
14.	**publication.date** \
    Publication date of the book, YYYY-MM-DD format;
15.	**first.print** \
    Year in which the first print appeared;
16.	**publisher** \
    Publishers of the books;
17.	**word.count** \
    Word count, or total number of words (tokens) used in a book;
18.	**type.count** \
    Total number of unique words (types) used in book;
19.	**sentence.length.mean** \
    Average sentence length in a book (in words);
20.	**sentence.length.variance** \
    Standard deviation of the sentence lenght;
21.	**paragraph.count** \
    Total number of paragraphs in a book;
22.	**sentence.count** \
    Total number of sentences in a book;
23.	**paragraph.length.mean** \
    Average paragraph length in a book (in words); 
24.	**raw.TTR** \
    Lexical diversity, or type-token ratio, which gives an indication of how diverse the word use in a book is;
25.	**sampled.TTR** \
    Unlike the raw type-token ratio, the sampled TTR is significantly more resistant to text size, and thus it should be preferred over the raw TTR. 


### reviews.csv
The 'reviews' dataset contains four different ratings that were given to 401 different books. The following is a list with the different column names and an explanation of what information they contain:

1.	**respondent.id** \
	Unique number for each respondent of the survey;
2.	**book.id** \
	Unique number to identify each book;
3.	**quality.read** \
	Rating on the quality of a book that a respondent has read Scale from 1 - 7, with 1 meaning 'very bad' and 7 meaning 'very good';
4.	**literariness.read** \
	Rating on how literary a respondent found a book that s/he has read. Scale from 1 - 7, with 1 meaning 'not literary at all' and 7 meaning 'very literary';
5.	**quality.notread** \
	Rating on the quality of a book that a respondent
 	has not read. Scale from 1 - 7, with 1 meaning 
 	'very bad' and 7 meaning 'very good';
6.	**literariness.notread** \
	Rating on how literary a respondent found a book that s/he has not read. Scale from 1 - 7, with 1 meaning 'not literary at all' and 7 meaning 'very literary';
7.	**book.read** \
    1 or 0: 1 indicates that the respondent read the book, 0 indicates the respondent did not read the book but had an opinion about the literary quality of the book.




### respondents.csv
The 'respondents' dataset contains information on the people that participated in the survey. This is a list with the different column names and an explanation of what information they contain:

1.	**respondent.id** \
Unique number for each respondent of the survey;
2.	**gender.resp** \
Gender of the respondent: Female, Male, NA;
3.	**age.resp** \
Age of the respondent;
4.	**zipcode** \
Zip code of the respondent;
5.	**education** \
Education level, containing 8 levels:
    1. "none/primary school" 
    2. "LBO|VBO|MBO (kader of beroeps)|MBO 1"
    3. "VMBO (theoretisch/gemengd)" 
    4. "MBO 2, 3, 4" 
    5. "HAVO|VWO|HBS|MMS" 
    6. "HBO" 
    7. "university" 
    8. "NA" 
6.	**education.english** \
English translation of education levels.
7.	**books.per.year** \
Number of books read per year by each respondent;
8.	**typically.reads** \
Typical genre of books that a respondent reads, with three levels a) Fiction; b) Non-fiction;c) both;
9.	**how.literary** \
Answer to the question 'How literary a reader do you consider yourself to be?', where respondents could fill in a number from 1 - 7, with 1 meaning 'not literary at all' and 7 meaning 'very literary';
10.	**s.4a1** \
Answer to the question: 'I like reading novels that I can relate to my own life'. Scale from 1 - 5, with 1 meaning 'completely disagree', and 5 meaning 'completely agree';
11.	**s.4a2** \
Answer to the question: 'The story of a novel is what matters most to me'. Scale from 1 - 5; 
12.	**s.4a3** \
Answer to the question: 'The writing style in a book is important to me'. Scale from 1 - 5;
13.	**s.4a4** \
Answer to the question: 'I like searching for deeper layers in a novel'. Scale from 1 - 5;
14.	**s.4a5** \
Answer to the question: 'I like reading literature'. 
Scale from 1 - 5;
15.	**s.4a6** \
Answer to the question: 'I read novels to discover new worlds and unknown time periods'. Scale from 1 - 5;
16.	**s.4a7** \
Answer to the question: 'I mostly read novels during my vacation'. Scale from 1 - 5;
17.	**s.4a8** \
Answer to the question: 'I usually read several novels at the same time'. Scale from 1 - 5;
18.	**s.12b1** \
Answer to the question: 'I like novels based on real events'. Scale from 1 - 5;
19.	**s.12b2** \
Answer to the question: 'I like thinking about a novel's structure'. Scale from 1 - 5;
20.	**s.12b3** \
Answer to the question: 'The writing style in a novel is of more importance to me than its story'. 
Scale from 1 - 5;
21.	**s.12b4** \
Answer to the question: 'I like to get carried away by a novel'. Scale from 1 - 5;
22.	**s.12b5** \
Answer to the question: 'I like to pick my books from the top 10 list of best sold books'. Scale from 1 - 5;
23.	**s.12b6** \
Answer to the question: 'I read novels to be challenged intellectually'. Scale from 1 - 5;
24.	**s.12b7** \
Answer to the question: 'I love novels that are easy to read'. Scale from 1 - 5;
25.	**s.12b8** \
Answer to the question: 'In the evening, I prefer to read books over watching TV'. Scale from 1 - 5;
26.	**remarks.survey** \
Any additional remarks that respondents filled in at the end of the survey;
27.	**date.time** \
Date and time of the moment a respondent filled in the survey, format in YYYY-MM-DD HH:MM:SS;
28.	**week.nr** \
Number of week in which the respondent filled in the survey;
29.	**day** \
Day of the week in which the respondent filled in the survey.


### motivations.csv
The 'motivations' dataset contains all motivations that people provided about why they gave a certain book a specific rating. The motivations have been parsed to provide POS tag information. The following is a list with the different column names and an explanation of what information they contain:

1.	**motivation.id** \
Unique number for each motivation given;
2.	**respondent.id** \
Unique number for each respondent;
3.	**book.id** \
Unique number of the book the motication pertains to;
4.	**paragraph.id** \
Number of paragraph within the motivation;
5.	**sentence.id** \
Number of sentence within the paragraph;
6.	**token** \
Token (in sentence order);
7.	**lemma** \
Lemma of token;
8.	**upos** \
POS tag of token;


### frequencies.csv
This is a table containing numerical values for word frequencies of the 5000 most frequent words (in a descending order of frequency) of 401 literary novels in Dutch. The table contains relative frequencies, meaning that the original word occurrences from a book were divided by the total number of words of the book in question.

The column names coincide with the column short.title from the `books.csv` data. The column rows list the 5000 most frequent words in the corpus. 


## General info

**Karina van Dalen-Oskam** (2023). _The Riddle of Literary Quality: A Computational Approach._ Amsterdam University Press.

**Karina van Dalen-Oskam** (2021). _Het raadsel literatuur. Is literaire kwaliteit meetbaar?_ Amsterdam University Press.

**Maciej Eder, Saskia Lensink, Joris van Zundert, Karina van Dalen-Oskam** (2022). “Replicating The Riddle of Literary Quality: The litRiddle package for R”, in: _Digital Humanities 2022 Conference Abstracts._ The University of Tokyo, Japan, 25–29 July 2022, p. 636-637 https://dh2022.dhii.asia/dh2022bookofabsts.pdf

**Corina Koolen, Karina van Dalen-Oskam, Andreas van Cranenburgh, Erica Nagelhout** (2020). Literary quality in the eye of the Dutch reader: The National Reader Survey. _Poetics_ 79: 101439, https://doi.org/10.1016/j.poetic.2020.101439.


More publications can be found at [https://literaryquality.huygens.knaw.nl/?page_id=588](https://literaryquality.huygens.knaw.nl/?page_id=588)

