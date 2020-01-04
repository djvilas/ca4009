# CA4009 – Search Technologies 2019 Exam Paper

## Section B

### QUESTION 2 [Total marks: 25]

## 2(a) [4 Marks]

> What are the differences between HTML and XML document markup? Use examples to illustrate your answer.

##### XML and HTML were designed with different goals:
- XML was designed to describe data and to focus on what data is.
- HTML was designed to display data and to focus on how data looks.

XML markup adds information to a document to make enhance its
usefulness.
HTML is about displaying information, XML is about describing information.

##### Differences:
- Some HTML elements do not require a closing tag, buut all XML elements must have a closing tag.
- XML tags are case sensitive, HTML tags are not.
- HTML tags are predefined, XML tags are user defined.

## 2(b) [6 Marks]

> i. What is meant by “human-in-the-loop” in image and video search?

##### Human-in-the-loop refers to an actual person helping to improve query results by manually providing relevance feedback.
- User enters their best attempt at a text or visual query.
- Collects the search results, and provides feedback on the relevance
of the retrieved content.
- Query is adapted via relevance feedback, and the user searches
again.
- Continues iteratively as the user steers the system towards relevant
terms.

> ii. What is the “semantic gap” in search of visual media? Why does the se-
mantic gap pose a challenge for multimedia search systems?

##### The semantic gap refers to the gap between the contents of a multimedia data stream and its meaning as interpreted by human observers.

It is relatively easy to extract low level features from visual images, e.g.
- The colours present in an image.

but very much harder to automatically describe images in the way that a human observer would.

###### This difference between machine and human descriptions of visual
media is referred to as the semantic gap.

##### There is a much larger gap between the features of a video which can be extracted automatically (as described in these notes) and its meaning or semantic interpretation by a user.

## 2(c) [4 Marks]

> How can XML be used for content annotation in multimedia information retrieval for
items such as images and video? Use examples to illustrate your answer.

#### XML DTDs can be defined for objects to be entered into a search engine.
For example, for a photo or other image, an XML markup scheme can be defined which captures the attributes of the image.
- Time of capture: day, month, year, minutes, hours, seconds, ...
- GPS location: mapped to named locations via gazzateer.
- Automatic content analysis (colours, shapes, named places, named
individuals, etc.)

#### Structured image metadata of this type can be used in various ways by a search engine:
- Search against individual elements, e.g. search for images taken only by a certain make or model of camera, or by using the description of the images entered when they were uploaded to an archive.
- Combine all metadata into a single unstructured file, index like a standard free text document, and then search using a standard information retrieval system.

## 2(d) [8 Marks]

> Before it can be searched, a collection of video recordings must be analysed to identify its visual and audio features. These extracted features for the video are then entered into a multimedia search system.

Outline a range of analysis techniques that can be applied to the visual and audio content of a video, such as a television news broadcast or sports match, to prepare it for indexing by an interactive video search system.
