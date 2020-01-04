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

