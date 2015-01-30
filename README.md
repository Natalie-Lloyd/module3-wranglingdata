Module 3 _Wrangling Data_
=====================

In the previous module, we successfully grabbed *lots* of data from various online repositories. Some of it was already in well-structured tables; much of it was not. All of it was text though. Initially, it (or most of it) was just scanned images of documents. At some point, _object character recognition_ was used to identify the black dots from the white dots in those images, to recognize the patterns that make up letters, numbers, and punctuation. There are commercial products that can do this (and we have some installed in the Underhill Research Room that you can use), and there are [free products that you can install](http://electricarchaeology.ca/2014/07/15/doing-ocr-within-r/) on your computer to do it yourself.

It all looks so neat and tidy. Ian Milligan discusses this ['illusionary order'](http://utpjournals.metapress.com/content/k002j61230g4556w/?p=8d64dca8cfec44e8b4858483ebf23daf&pi=2) and its implications for historians:
>In this article, I make two arguments. Firstly, online historical databases have profoundly shaped Canadian historiography. In a shift that is rarely – if ever – made explicit, Canadian historians have profoundly reacted to the availability of online databases. Secondly, historians need to understand how OCR works, in order to bring a level of methodological rigor to their work that use these sources.

Just as we saw with Ted Underwood's article on [theorizing search](http://www.jstor.org/stable/10.1525/rep.2014.127.1.64), these 'simple' steps in the research process are anything but. They are also profoundly theoretical in how they change what it is we can know. In archaeology, every step of the method, every stage in the process, has a profound impact on the stories we eventually tell about the past. Decisions we make destroy data, and create new data. Historians aren't used to thinking about these kinds of issues!

There are also _manual_ ways of doing the same thing as OCR does - we call these things 'humans', and we organize their work through 'crowdsourcing'. We break the process up into wee manageable steps, and make these available over the net. Sometimes we gamify these steps, to make them more 'fun'. If several people all work on the same piece of text, the thinking is that errors will cancel each other out: a proper transcription will emerge from the work of the crowd. Take a look at these two pieces concerning the [_Transcribe Bentham_](http://www.transcribe-bentham.da.ulcc.ac.uk/td/Transcribe_Bentham) project:

+ Causer & Wallace, [Building A Volunteer Community: Results and Findings from Transcribe Bentham](http://www.digitalhumanities.org/dhq/vol/6/2/000125/000125.html) DHQ 6.2, 2012
+ Causer, Tonra, & Wallace [Transcription maximized; expense minimized? Crowdsourcing and editing The Collected Works of Jeremy Bentham](http://llc.oxfordjournals.org/content/27/2/119.abstract)LLC 27.2, 2012

While transcriptions might've provided the earliest examples of crowdsourcing research (but see also [The HeritageCrowd Project](http://quod.lib.umich.edu/d/dh/12230987.0001.001/1:9/--writing-history-in-the-digital-age?g=dculture;rgn=div1;view=fulltext;xc=1#9.3) and the subsequent ['How I Lost the Crowd'](http://electricarchaeology.ca/2012/05/18/how-i-lost-the-crowd-a-tale-of-sorrow-and-hope/)), other tasks are now finding their way into the crowdsourced world - see the archaeological applications within the [MicroPasts](http://micropasts.org/) platform. These include things like 'masking' artefact photographs in order to develop 3d photogrammetric models.

### Exercises

In the exercises for this week we are going to focus on some bare-bones wrangling of data. First, we are going to transcribe and mark up some text that has already been digitized (in the sense that there exists a digital image). If you've done HIST2809 with me, this will feel rather familiar - but instead of making a transcription that sits in our notebook, we'll make one that lives online. Since it is online, the use of xml tags like <date> or <advertisement> etc allow us to do some other quite interesting things. We'll look at M. Beal's Colonial Newspaper Database in more detail. This will introduce us to the 'Text Encoding Initiative' and some of the scholarly work surrounding making scholarly editions online. Some of you might be interested in how all of this ties into *linked data*, so I'll provide further resources to that world for those who wish to go exploring.

Then, we'll switch gears and we'll use *regular expressions* to search and extract information from the Diplomatic Correspondence of the Republic of Texas, which you'll find at the Internet Archive. If you're on a PC, download [Notepad++](http://notepad-plus-plus.org/) - this is a souped-up version of the simple notepad application, and allows us to do very useful things indeed. If you're on a Mac, TextWrangler is probably already installed and is all you need. If you're working in Linux, you can use whatever text editor you're familiar with.

We'll conclude by using 'Open Refine' to tidy up the information we extracted from the Texan correspondence. 

### Things you will learn in this module:

+ the basic concepts of XML and TEI for marking up text
+ the power of regular expressions. 'Search' and 'Replace' in Word just won't cut it any more for you! (Another reason why you should write in Markdown in the first place and then convert to Word for the final typesetting - Indeed, there will be an optional exercise to install and use [Pandoc](http://johnmacfarlane.net/pandoc/demos.html) to convert your .md files to .docx).
+ Open Refine as a powerful engine for tidying up the messiness that is ocr'd text.
