# CA4009 – Search Technologies 2019 Exam Paper

# QUESTION 2 [Total marks: 25]

## 2(a) [4 Marks]

> What are the differences between HTML and XML document markup? Use examples to illustrate your answer.

### XML and HTML were designed with different goals:
- XML was designed to describe data and to focus on what data is.
- HTML was designed to display data and to focus on how data looks.

XML markup adds information to a document to make enhance its
usefulness.
HTML is about displaying information, XML is about describing information.

### Differences:
- Some HTML elements do not require a closing tag, buut all XML elements must have a closing tag.
- XML tags are case sensitive, HTML tags are not.
- HTML tags are predefined, XML tags are user defined.

## 2(b) [6 Marks]

> i. What is meant by “human-in-the-loop” in image and video search?

### Human-in-the-loop refers to an actual person helping to improve query results by manually providing relevance feedback.
- User enters their best attempt at a text or visual query.
- Collects the search results, and provides feedback on the relevance
of the retrieved content.
- Query is adapted via relevance feedback, and the user searches
again.
- Continues iteratively as the user steers the system towards relevant
terms.

> ii. What is the “semantic gap” in search of visual media? Why does the se-
mantic gap pose a challenge for multimedia search systems?

### The semantic gap refers to the gap between the contents of a multimedia data stream and its meaning as interpreted by human observers.

It is relatively easy to extract low level features from visual images, e.g.
- The colours present in an image.

but very much harder to automatically describe images in the way that a human observer would.

### This difference between machine and human descriptions of visual media is referred to as the semantic gap.

### There is a much larger gap between the features of a video which can be extracted automatically (as described in these notes) and its meaning or semantic interpretation by a user.

## 2(c) [4 Marks]

> How can XML be used for content annotation in multimedia information retrieval for
items such as images and video? Use examples to illustrate your answer.

### XML DTDs can be defined for objects to be entered into a search engine.
For example, for a photo or other image, an XML markup scheme can be defined which captures the attributes of the image.
- Time of capture: day, month, year, minutes, hours, seconds, ...
- GPS location: mapped to named locations via gazzateer.
- Automatic content analysis (colours, shapes, named places, named
individuals, etc.)

### Structured image metadata of this type can be used in various ways by a search engine:
- Search against individual elements, e.g. search for images taken only by a certain make or model of camera, or by using the description of the images entered when they were uploaded to an archive.
- Combine all metadata into a single unstructured file, index like a standard free text document, and then search using a standard information retrieval system.

## 2(d) [8 Marks]

> Before it can be searched, a collection of video recordings must be analysed to identify its visual and audio features. These extracted features for the video are then entered into a multimedia search system.
Outline a range of analysis techniques that can be applied to the visual and audio content of a video, such as a television news broadcast or sports match, to prepare it for indexing by an interactive video search system.

- Multimedia content is often accompanied by text metadata which can be used to search for relevant items without requiring analysis of the multimedia content.

### Automatic speech reconition (ASR) systems can be used to generate imperfect index information for spoken content. Index errors arising from ASR errors will reduce effectiveness of a retrieval system, but overall retrieval is often good enough to be useful.
Automatic speech recognition (ASR) is hard!
- Speech patterns of different people show significant variations.
- Every individual utterance of a word by every speaker is unique.
- Speech is continuous – often with no gaps between spoken words.
- Words are “smeared” together.

### Content-based retrieval of visual media is a much more challenging prospect than spoken content retrieval.

###Fundamental questions include:
- What visual features should be extracted to describe the content to be
retrieved?
- Can these features be extracted reliably?
- How should queries be posed

### Successful content-based retrieval systems for visual media have generally been task or domain specific, i.e.
- They are developed for a specific activity such as spotting cars in a video or tracking football players in match.
- They can often be adapted for use in different domains, e.g. to track aeroplanes or baseball players.

### Relevant images can be located using a variety of attributes. These can include automatically extracted and manually assigned features.

- Using Colour Histograms
- Texture-Based Retrieval
- Shape-Based Retrieval
- For most effective access an application should generally use both the video and audio media synchronised for retrieval.

## 2(e) [3 Marks]

> Suggest how multiple audio and visual features extracted from a video could be combined to identify an event in the video, e.g. a goal in a soccer match, a wedding in a movie, or the key points in a scientific lecture.

### Using 'a goal in a soccer match' as an example, by using color histograms and shape-based retrieval, we are able to track the ball on a soccer field. We can do the same for the goal. If these two objects interact, we then analyse the audio to look if there was a loud cheer in the crowd. This would indicate that a goal has been successfuly completed, and that the ball did not miss.

# QUESTION 4 [Total marks: 25]

## 4(a) [4 Marks]

> Give three examples of English stop words, and explain why they are stop words. Why are stop words often removed in information retrieval systems?

### Frequent words are shown to have low resolving power and intuitively are not of much benefit to the IR process, they can thus be removed during indexing without impacting on retrieval effectiveness.

### Stop words are typically prepositions and conjunctions, e.g. the, of, in, a, and, to, an.

## 4(b) [5 Marks]

> What are stemming algorithms as used in automatic indexing for information retrieval?

### Stemming is one example of a conflation procedure that is designed to bring together words that are related to each other in some way, e.g. stop, stopping, stops, stopped → stop

### Stemming algorithms are designed to remove suffixes that inhibit matching.
### A stemming algorithm operates by:
- Matching the ending of a word against a suffix directory.
- Removing any suffix that is identified.
- Checking whether any context-sensitive rules apply.

> Explain what is meant by under-stemming and over-stemming.

### Over-stemming is when two words with different stems are stemmed to the same root.
- MEDICAL → MED
- MEDIA → MED
- MEDIAN → MED

### Under-stemming is when two words that should be stemmed to the same root are not.
- GASES → GAS 
- GAS → GA 
- GASEOUS → GASE 

> For stemming of English language text, why do we generally want to stem suffixes, but not prefixes?

### In English, we would generally regard only those differing in their suffix as semantically similar.

## 4(c) [7 Marks]

> i. Why is the use of suitable data structures vital for the implementation of
effective search systems.

### An important feature for useres of an ir system is often the time taken for it to respond to their search request. An important factor in determining the speed of an IR System response is the strcuture of the document representations. So, we want a data structure that will minimise the computational cost, and hence maximise the efficiency and speed of the query-document matching operation when a new request is entered.

> ii. Using an example, explain the use of inverted files in text search systems. Your answer should illustrate how hashing is used for efficient processing of search terms.

### Suppose that a document archive consists of just 3 documents represetned only by their titles.

- D1. Information retrieval systems
- D2. Databse management systems
- D3. Retrieval of information from computer systems

### After removing stop words, each remainign word is tokenized.
- computer -> T1
- database -> T2
- information -> T3
- management -> T4
- retrieval -> T5
- systems -> T6

### Represent the documents in an inverted file organization produces:
- T1 -> D3
- T2 -> D2
- T3 -> D1, D3
- T4 -> D2
- T5 -> D1, D3
- T6 -> D1, D2, D3

### Potentially relevant matching documents are identified using the list of terms.

- The term data in the inverted file can be extended to include the location of each term within each document, although adding this information will make the inverted file larger.
- This can be used to incorporate term proximity into retrieval matching functions.
- Storing proximity information can also allow for phrasal searching.

## 4(d)
### [4 Marks]
> i. What is enterprise search? Why is enterprise search of increasing importance?

### Enterprise Search refers to the application of search technologies to information within an organisation, e.g. a business or public body. Interestingly something like 80% of enterprise content is in unstructured form, i.e. not in a structured database!
### There is evidence that employees spend a significant amount of time searching for information needed in their work, and often failing to find it!

### [5 Marks]
> ii. Metadata can be used to annotate enterprise content with facets relating to the content items. Give three examples of typical facets in enterprise content.

### Each facet typically corresponds to the possible values of a property common to all objects.
- Author
- Language
- Source

> How can facets be used to support search of partially remembered content in enterprise search in combination with suitably designed rich user interfaces, to facilitate effective enterprise search?

### Faceted search can ber useful since the searcher may remember one or more details of the item that they are looking for, even if they can't remember enough details to create a meaningful search query. e.g. They may remember that they received an email that they are looking for from a particular person.
### Thus they could start their search by looking at items from said person only.

# QUESTION 5 [Total marks: 25]

## 5(a) [3 Marks]

> What is the purpose of an information retrieval system? How does a standard information retrieval system attempt to achieve this purpose?

### The purpose of an information retrieval system is to satisfy a user's information need. The IR system seeks to locate documents relevant to this information need.
### A standard IR system attempts to do this based on the relationship between the contents of the user's search request and each potentially relevant document which is available in a document collection. Other factors can also be used, such as...
- Hypertext structures
- Popularity with other searches
- Quality of content
- Recency of updates

## 5(b) [8 Marks]
> The Okapi BM25 term weighting function for best-match information retrieval is given by the following equation (refer to exam paper).
With reference to the Okapi BM25 model as described by the equation above, explain the concept of:
> - Collection frequency weighting
> - Term frequency weighting
>- Document length normalisation

> How do the k1 and b factors operate in the equation for the Okapi BM25 model?

### Collection Frequency Weighting -> Terms that occur in fewer documents are often more valuable than ones which occur in many documents.

### Given:
> _t(i)_ = Term

> _n(i)_ = The number of documents term _t(i)_ occurs in

> _N_ = The total number of documents in the collection archive

> The _CFW_ for term _t(i)_ is
> _cfw(i) = log (N / n(i))_

### Term Frequency Weighting -> The more often a term occurs in a document, the more likely it is to be important for that document. This refers to the term's within-document frequency.

> The term frequency for term _t(i)_ in document _d(j)_ is:
tf(i,j) = the number of occoruences of term _t(i)_ in document _d(j)_.

### Document Length Normalisation -> A term that occurs the same number of times in a short document and in a long document, is likely to be more valuable for the former. 

>Without compensating for document length, longer documents will tend to have higher matching scores merely because they are long.
>Document length of document _d(j)_ is...
_dl(j)_ = The total number of term occurences in document _d(j)_

>Normalised average document length:
_ndl(j)_ = _dl(j)_ / average _dl_ for all documents

### K1 and B
- The _k1_ factor determines the impact of term frequency in a document. A typical value for _k1_ would be 1.5
- _b_ determines the degree of document length normalisation. The value of _b_ can vary in range of 0 to 1.

## 5(c) [5 Marks]
> Knowledge graphs encode information extracted from source texts. A knowledge graph typically describes the relationships between entities and the attributes of the entities.
Give a sample example and illustrate these features of a knowledge graph.

![Obama's Knowledge Graph](https://github.com/djvilas/ca4009/blob/master/obama.PNG "Obama's Knowledge Graph")

## 5(d)
### i. [4 Marks]
> What is the difference between a conventional information retrieval system and a question answering system?
Even if high quality question answering systems were available commercially, why would there still be a need for information retrieval systems?

### Information retrieval systems are concerned with searching for and retrieving documents relevant to a user's information need. The searcher is required to extract information from the retrieved documents in order to satisfy their information need.

### However, many user requests are essentially questions looking for a single fact or piece of information that ca be made in a short statement.

### Even if high quality question answering systems were available commercially, we would still need information retrieval systems to initially find relevant documents, and then for those who want to expand upon their answer you would need to provide broader information.

### ii. [5 Marks]
> Sketch the standard workflow of a question answering system based on document retrieval.
![IR-Based Question Answering Graph](https://github.com/djvilas/ca4009/blob/master/answering.PNG "IR-Based Question Answering Graph")

> Suggest how a knowledge graph could be used for question answering instead of retrieving documents.

- Process the question to determine the EAT (Expected Answer Type). Eg, Who is the President of Ireland? EAT = Name
- Analyze the documents to try to find potential answers that match this type of requirement.

# QUESTION 6 [Total marks: 25]

## 6(a) [6 Marks]
> Explain the following concepts as they apply to the goals of an operational recommender system: relevance, novelty, serendipity, diversity.

- Relevance: Recommend items relevant to the user.
- Novelty: Recommend new items relevant to the user which they have not seen before.
- Serendipity: Recommend unexpected or surprising items which the user finds relevant.
- Diversity: If a diverse list of items are arecommended, there is a greater chance that one of them will be relevant to the user, and therefore be purchased.

> Why is a successful recommender system likely to incorporate all of these facotrs in determining its output?

### All of the goals above are designed to maximise profits.

## 6(b) [4 Marks]

> i. What is the cold start problem in recommender systems?
> ii. How does the cold start porblem pose a challenge for new items introduced into the catalogue of an e-commerce website?

- User-side problem: Relates to the difficulty of making recommendations for new users who ave so far provided little rating information.
- Item-side problem: Where new items have not been rated often enough to make reliable recommendations - generally they will not be recommended very often, and so will not build up rating information.

## 6(c) [6 Marks]
> What are the features of a knowledge-based recommender system?
- KBRSs make recommendations based on customer requiremements and item descriptions, or use of constraints to specify user requirements.
- Knowledge-bases contain data about rules and similarity functions for the matching process.
- KBRSs allow the user to explicitly specific what they want.

> For what tasks are knowledge-based recommender systems well suited?

- Useful for items purchased infrequently as sufficient ratings are typically not available for these items to make reliable recommendations to a user using other methods.

> Why would a content-based recommender system or collaborative filtering approach not be suitable for these tasks?
- A CBRS combiens rating of previous items by the user, their selection or purchase behaviour and analysis of the contents of items to recommend items. These recommendations will be similar to other purchases are already made, but will not be specifically what the user goes out to look for.
- A CF system recommends items based on other people's ratings to find other users who are similar to you. These recommendations widely vary and will not be specific to a users then and there needs.

## 6(d) [3 Marks]
> What is A/B testing as applied to online web applications?

### When trying to test out a tweak or a new algorithm for a search engine that is live and available for public use, you can get very quick feedback on how well your updated system performs comapared to the previous version.
### Consider A to be your current system, and B will be the system with a tweak that should improve the user's experience. Both A and B search engines are launched live at the same time. They both look and function as far the user is concerned, identically. They have no knowledge of there existing two slightly different search engines. Users are randomly assigned either A or B engine. Based on a user's interactivity, you can track how many clicks were made, how many searches/alterations, etc. to figure out whether the newer system B outperformed A.

## 6(e) [6 Marks]

> i. Summarization is content reduction through selection or generalisation on what is important in the source. Using an example, explain what is meany by the concepts of selection and generalisation in this definition.

- Selection -> Forming a summary focused on a subset of the topical content of the source document in detail.
- Generalisation -> Forming a summary which overviews the entire topical contents of the source document.

