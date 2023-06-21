# Data Info File for litRiddle R-package

This file provides information on the provenance and creation of the data provided in this repository.

Most details of the process of creation of the data can be found in the following publication:

**Karina van Dalen-Oskam** (2023). _The Riddle of Literary Quality: A Computational Approach._ Amsterdam University Press.

The table `books` contains a number of additional columns on word and sentence metrics, not described in the publication above, to wit:

17. word.count                Word count, or total number of words (tokens)
                              used in a book;
18. type.count                Total number of unique words (types) used in book;
19. sentence.length.mean      Average sentence length in a book (in words);
20. sentence.length.variance  Standard deviation of the sentence length;
21. paragraph.count           Total number of paragraphs in a book;
22. sentence.count            Total number of sentences in a book;
23. paragraph.length.mean     Average paragraph length in a book (in words); 
24. raw.TTR                   Lexical diversity, or type-token ratio, which 
                              gives an indication of how diverse the word use 
                              in a book is;
25. sampled.TTR               Unlike the raw type-token ratio, the sampled 
                              TTR is significantly more resistant to text 
                              size, and thus it should be preferred over the 
                              raw TTR. 

Metrics listed here were inferred from the full texts of the novels. The full text files used have one paragraph per text line. Additional metrics were inferred by using [spaCy](https://spacy.io/) (version 3.5.3) to parse the full texts of the novels using, which yields lemma, sentence boundary, and token information. For Dutch novels spaCy's model `nl_core_news_sm` was used. 

--
