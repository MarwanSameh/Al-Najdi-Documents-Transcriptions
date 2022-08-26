# 📝 Al-Najdi-Documents-Transcriptions

## Overview
This repository is the collection of transcribed documents of the Al-Najdi family. The Documents have been collected, scanned, and transcribed to be machine readable and usable in research. The repository is new and is being updated regularly with new collections of documents.


## 🛠 Tools
- XML
- XSLT
- TEI
- CSS
- HTML


## 🧮 Using the Repository
- To view the transcribed documents, navigate to documents and view the PDF or HTML file of your choice.
- To view the XML TEI navigate to documents/XML and pick the filr of your choice
- You can clone the repository and edit the XSLT or CSS file.
- There are some templates available to use (some are more finicky than others - standard Oxygen s the safest option).


## 🕶 Reflection on the Process
Throughout the past few months, I have been intrigued by the cultural role that typical day-to-day documents play in creating cultural heritage. From FMCGs (fast-moving consumer goods) to documents and money, seemingly useless pieces of paper have intrinsic value. The idea of encoding old documents become even more interesting when my parents showed me some of the old documents my grandparents had.

Old documents give the reader an insight into what the lives of those people were like. It included some of the trade they did, how much they paid for things, buying pieces of land, and small details that no one would hear about unless they are told.

I felt there is a window to start recording seemingly unimportant pieces of family history: contracts, IDs, and even birth certificates. These small pieces of information, when collected and analyzed as a whole, might add another layer of understanding to the holistic understanding of the culture and daily practices of people at a certain point in time.


## A Personal Reason
Our family likes to save documents and share them with later generations. From old photographs to 3.5mm cinema reels, to books and handwritten notes, our family loves saving these things. But losing things along the way is inevitable, and I always felt so sorry about losing such valuable things. They often get sold in bulk to antique/junk dealers, or even worse, stolen to never be returned. Yet calculating the value to family – even more cultural – heritage, these “antiques” become priceless. Some of these documents start to degrade, as they were not built to last a lifetime.

When I first got my great grandfather’s documents from my grandmother in 2018, I didn’t think much of it more than that the documents looked “cool”. It wasn’t until later that I was interested in learning more about the document and what is behind it. As I haven’t met my great grandfather “Ali Al-Najdi”, I was not interested in knowing much about him. Although my grandfather used to talk about how he lived his life and how his parents were, I didn’t think much of it. After my grandfather passed away in late 2020, I started thinking about all the stories he used to tell, things I no longer remember.


## Designing a Solution to Avoid Losing Information
When I started this MA program at UCC, I got introduced to transcription and encoding of old documents. The idea of encoding the stories my parents tell me about my grandparents started becoming more exciting and thought of ways to record this information before it gets lost down the later generations.

The first thing I needed to think about was transcribing the document. I started thinking about XML/TEI as a good starting point. The transcription method is mature and breaks down information into machine-readable pieces. The TEI schema also gives the transcriber the freedom to add corrections and notes without destroying the original flow of information in the document.

I thought of ways to start the transcription, but the easiest way that I could find was just writing everything in an MS Word document and then taking it from there into the code editor. I was not comfortable enough with TEI either, and there were lots of things that I did not know how to make work, so I had to put in the time to learn TEI.

I also thought of other ways to display the content. I wanted to create a transcribed document with the original scan of the document beside it. I also wanted to add English and Arabic versions of the transcriptions on the left side of the scanned document for the user to choose between. Finally, I wanted to add connections between the image and the scanned image.

So the plan was to transcribe and translate the content in MS Word, convert the transcription/translation into TEI, and add the image beside the content.


## Implementing the Plan
The first step was transcribing the content. While seemingly easy in the beginning, some regions of the text were almost unreadable to me in the beginning. The way of writing used in the document is very scriptive and no longer used in day-to-day documents. What made this worse is that the writer had very compact/unreadable handwriting in some parts where elements overlapped. Another issue was the language used. Some words used within the text are no longer in use. The way the writer wrote the month of April as “Bril/بريل” was very confusing.

The transcription took me days and needed a lot of help from many people (mainly family members). Yet once it was transcribed once, I was able to read the text easily afterward. The change of typography through time and the role it has on later generations needs further research.

After finishing the transcription, I started translating the content. While some regions of the translation were easy, other regions/words had no exact English equivalent. Moreover, I translated the text word for word, which made some parts of the text not as easy to comprehend (side note: something I would change if I had more time is to add two versions of the translation where one takes a word-for-word approach while the other focuses on holistic meaning).

I then started using TEI to do the encoding, I found out that I needed to learn a lot, especially when it comes to embedding images in the document. I wanted to create a custom look for the document and looked for other XSLT templates to enhance the look. But I later stuck to the safest option of using the standard Oxygen editor TEI XSLT template. I tried using other boilerplate templates, but they didn’t work well with all the TEI tags. I tried getting into IIIF (International Image Interoperability Framework) but was unable to get it to work within the timeframe. What I was able to do is embed the image in the XML file but faced the issue of the image not showing. Whenever I embedded a <facsimile> tag, the image was displayed as a link. Something I would like to try is to add multiple pages and see if the result would be any different.
  
    <facsimile>
        <surface>
            <graphic url="../../../Encoding/documents/Images//Birth_Certificate_Small.jpg" n="1r"/>
            <zone xml:id="mohammedElnagdy" lry="486" lrx="1210" uly="366" ulx="703"/>
            <zone xml:id="matareyaBureau" lry="403" lrx="1526" uly="283" ulx="1183"/>
        </surface>
    </facsimile>
  
One more issue was trying to target zones and link those zones to the encoding (as some sort of annotating). While the zones worked (but only within the Oxygen editor), there was no visible link between the encoding and the image.

  
## Analyzing the Birth Certificate
After transcribing, translating, and encoding the document, I wanted to add more pieces of information using the TEI format. I started by gathering small pieces of information that fit within the birth certificate. I talked to family members and collected a large sum of information that would have been lost unless they were recorded. I later only used the relevant pieces of information to build a description and breakdown of the document.
  
I started by mentioning information about the father (Mohammed Al-Najdi), mother (Zainab Al-Rayyes), and son (Ali Al-Najdi), such as their occupation, relation with each other, and dates of birth (only Ali’s was available).
  
I then added notes that explained some of the words mentioned within the document that mean something beyond the translation’s literal meaning. For example, "Al-Sayyed" in this context is not a name, but rather a title used to refer to a family name; the word is equivalent to "sir" in English.
I then started gathering information about the name Al-Najdi, simple history of the origin of the name and the place they lived in before coming to Egypt, and where Ali Al-Najdi and his family lived through a map.

  
## The Experience
Through this experience, I have learned how to use XML and TEI in practice, and the methods of transcription and translation. The process made me really appreciate the work that goes into transcription. While the process of learning through doing was hard, it was very enjoyable. A thing that I would change doing this again is trying out the technologies before I start implementing what I know. 

