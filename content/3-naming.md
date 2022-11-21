---
title: Step 3 - Naming
nav: true
topics: Content; Markdown; Includes
description: >
    This text is a "section description". Below is "section topics", followed by an example section video embed. This page details how to write content pages and add interest with includes.
youtubeid: moJgWrD6dwg
---

### Step 3
## Naming Conventions

If implemented early and consistently, a standardised system for naming files can:
- make file naming easier
- facilitate access, retrieval and storage of files
- improve efficience navigating files
- guard against misplacing or losing files
- assist with version control
- identify obsolete or duplicate records

## What is a File Naming Convention?

A File Naming Convention (FNC) is a system for naming your all your files to include a description of the contents and the context. This is a system that is best established as early as possible; ideally before collection research data.

## What is a File Name? 
***File names*** are simply those names that you must give when saving to any new file, and which are listed in the directory of a folder. The FNC is used at that stage with each file that forms any part of your research.

### What are the benefits of using a file naming convention? 
Naming files consistently, logically and in a predictable manner will prevent against unorganised files, misplaced or lost data.  It can also prevent backlogs or project delays by presenting a clear and real-time display of the current or completed work.

### Coming up with a plan for your team on how to name files.
Former PhD student and subsequent founder of the Figshare platform, Mark Hahnel, typified a common challenge: *‘During my PhD I was never good at managing my research data. I had so many different file names for my data that I always struggled to find the correct file quickly and easily when it was requested. My former PI was so horrified upon seeing the state of my data organisation that she held an emergency lab book meeting with the rest of my group when l was leaving’*. 
Research Information, April/May 2014  

Your research team should agree on the following elements of a file name prior to data collection:
* Vocabulary - choose a standard vocabulary for file names, so that everyone uses a common language
* Punctuation - decide when to use punctuation symbols, capitals and hyphens
* Dates - agree on a logical use of dates so that they display chronologically i.e. YYYY-MM-DD
* Order - confirm which element should go first, so that files on the same theme are listed together and can therefore be found easily
* Numbers - specify the amount of digits that will be used in numbering so that files are listed numerically e.g. 01, 002, etc.

As previously suggested, consistent and meaningful naming of files and folders can improve efficiency.  See this example below:

YYYYMMDD_SiteA_SensorB.CSV
Date  Location   Sensor
Which when applied, would look like this below
20150621_Yaouk_Humidity.CSV

Some characters may have special meaning to the operating system so avoid using these characters when you are naming files. These characters include the following: / \ " ' * ; - ? [ ] ( ) ~ ! $ { } &lt > # @ & | space tab newline https://www.ibm.com/support/knowledgecenter/en/ssw_aix_71/com.ibm.aix.osdevice/filename_conv.htm

The University of Edinburgh has a comprehensive and easy to follow list (with examples and explanations) of [13 Rules for file naming conventions](https://www.ed.ac.uk/records-management/guidance/records/practical-guidance/naming-conventions)

### Beginner
Consider some easy naming convention for your data files and documents. 
Any dates are best stored with YYYY-MM-DD because it can be re-ordered chronologically.
Avoid spaces in your file names because some applications do not support it.

### Intermediate
Make sure you follow 13 Rules for file naming conventions  https://www.ed.ac.uk/records-management/guidance/records/practical-guidance/naming-conventions

### Advanced
Do you have a policy in your team around naming conventions? If not, this is a great way of discussing the priorities of the research data.


### Internal Resources
* Talk to your Research Support Services librarian at library@griffith.edu.au


### External Resources
* [Naming things by Jenny Bryan](https://speakerdeck.com/jennybc/how-to-name-files)
* [File naming and folder conventions by CESSDA ERIC](https://www.cessda.eu/Training/Training-Resources/Library/Data-Management-Expert-Guide/2.-Organise-Document/File-naming-and-folder-structure)
* The University of Edinburgh has a comprehensive yet easy to follow list (with examples and explanations) of 13 Rules for file naming conventions https://www.ed.ac.uk/records-management/guidance/records/practical-guidance/naming-conventions
* Australian National Data Services (ANDS). (2018). ANDS Guide: File wrangling. Retrieved from https://www.ands.org.au/working-with-data/data-management/file-wrangling 

[Previous](https://guereslib.github.io/ten-repo/2-document) | [Home](https://guereslib.github.io/ten-repo/) | [Next Page](https://guereslib.github.io/3-folders)


## Content Pages

Content pages are written in markdown and can be enhanced using Liquid includes that are packaged with the template.
Start by editing the examples or creating new files in the "content" folder.

[Markdown](https://daringfireball.net/projects/markdown/) is a standard to [simplify writing](https://evanwill.github.io/_drafts/notes/writing-markdown.html) content for the web. 
[GitHub markdown flavor](https://help.github.com/articles/basic-writing-and-formatting-syntax/) can be used any where on GitHub and in Jekyll.
The basics are intuitive, you can learn in about a minute!
See [Markdown in a Minute](https://evanwill.github.io/_drafts/notes/markdown-minute.html) to get started.

At the top of each content page is "YAML front matter" used to configure the page.
Use these options:

- `nav:` add the text you want to appear in the the header and footer navigation. 
    - Alternatively, use `nav: true` to use the page's `title` value for the nav text. 
    - Do not include `nav` if you do not want the page to appear in the nav elements.
    - All pages with a `nav` value will appear in the header and footer navigation, sorted by order of filenames. For simplicity use leading numbers in the lesson page filenames to create correct order.
- `title:` value will appear as `h1` at the top of the page.
- `description:` will appear as an indented text block below the title (optional). This gives you a chance to summarize the section contents.
- `topics:` will appear as a small feature below the title or description (optional). These also appear in the default TOC.
- `youtubeid:` will add an YouTube video embed (optional). Find the id in the YouTube link. For example, in `https://youtu.be/moJgWrD6dwg` or `https://www.youtube.com/watch?v=moJgWrD6dwg` the youtubeid is `moJgWrD6dwg`.
- Alternatively, if you don't want `title` or other options to appear on the page, you can over ride the section layout by adding `layout: default` 

## Components Includes

`workshop-template-b` contains a series of [Liquid "includes"](https://jekyllrb.com/docs/includes/) to simplify adding basic [Bootstrap 5 components](https://getbootstrap.com/docs/5.0/components/) to your Markdown content.
The includes can be found in the "_includes" folder. 
Check the comments at the top of each include file for details about options and how to use them.

Examples below demonstrate the includes with sample include `code` followed by the rendered feature:

--------

### Figures 

- put any images you want to use in the "images" folder, or use a full URL to external images.
- in the markdown file where you want the image to appear, use the `figure.html` include on its own line, following the pattern: `{% raw %}{% include figure.html img="my-cat.jpg" alt="cat" caption="My cat" width="50%" %}{% endraw %}`
- figures will be centered, and can optionally be given a caption and percentage width.

Include code: 

`{% raw %}{% include figure.html img="uidaho-workshop.jpg" alt="workshop scene" caption="Library workshops!" width="75%" %}{% endraw %}`

Becomes:

{% include figure.html img="uidaho-workshop.jpg" alt="workshop scene" caption="Library workshops!" width="75%" %}

----------

### Alerts

Include code:

`{% raw %}{% include alert.html text="This is a Bootstrap [Alert](https://getbootstrap.com/docs/4.1/components/alerts/)" align="center" color="success" %}{% endraw %}`

Becomes:

{% include alert.html text="This is a [Bootstrap Alert](https://getbootstrap.com/docs/4.1/components/alerts/)" align="center" color="success" %}

-----------

### Link Buttons 

Include code:

`{% raw %}{% include button.html text="Bootstrap Docs" link="https://getbootstrap.com/docs/5.1/components/buttons/" color="info" %}{% endraw %}`

Becomes:

{% include button.html text="Bootstrap Docs" link="https://getbootstrap.com/docs/5.1/components/buttons/" color="info" %}

---------

### Cards

Include code:

```{% raw %}
{% capture text %}
1. Can add more complex text using markdown.
2. Use a Liquid capture to create the text.
3. It magically becomes a [Bootstrap Card](https://getbootstrap.com/docs/4.1/components/card/).
{% endcapture %}
{% include card.html text=text header="Example Card" title="Title example" img="uidaho-workshop.jpg" %}{% endraw %}
```

Becomes: 

{% capture text %}
1. Can add more complex text using markdown.
2. Use a Liquid capture to create the text.
3. It magically becomes a [Bootstrap Card](https://getbootstrap.com/docs/4.1/components/card/).
{% endcapture %}
{% include card.html text=text header="Example Card" title="Title example" img="uidaho-workshop.jpg" %}

------------

### Accordion

Include code:

`{% raw %}{% include accordion.html title1="Example section" text1=example1 title2="Section two" text2=example2 title3="Section three" text3=example3 %}{% endraw %}`

Becomes:

{% include accordion.html title1="Section one" text1="Some text content" title2="Section two" text2="Some text content" title3="Section three" text3="Some text content" %}

------------

### Modal

Include code:

`{% raw %}{% include modal.html button="Try Me" color="success" title="Example Modal" text="This is a modal, with little text." %}{% endraw %}`

Becomes:

{% include modal.html button="Try Me" color="success" title="Example Modal" text="This is a modal, with little text." %}

-------------

### YouTube embed

Include code:

`{% raw %}{% include video-embed.html youtubeid="moJgWrD6dwg" caption="Example video" %}{% endraw %}`

Becomes:

{% include video-embed.html youtubeid="moJgWrD6dwg" caption="Example video" %}

-------------

### Jumbotron

Include code:

`{% raw %}{% include jumbotron.html heading="Jumbotron Include" text="Paragraph content goes here." button-text="Learn more" button-color="outline-primary" button-link="https://github.com/evanwill/workshop-template-b" border=true %}{% endraw %}`

Becomes: 

{% include jumbotron.html heading="Jumbotron Include" text="Paragraph content goes here." button-text="Learn more" button-color="outline-primary" button-link="https://github.com/evanwill/workshop-template-b" border=true %}
