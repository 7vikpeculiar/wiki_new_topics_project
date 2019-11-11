---
layout: default
---

[Link to the code base](https://github.com/SanjanaSunil/ire-major-project).

# Overview

Wikipedia in Indian languages are not as well developed as the English
Wikipedia despite increase in usage. There are 1,33,944 articles in Hindi Wikipedia as compared to 59,64,000 articles in English Wikipedia. The focus of our project will be to identify new topics that could be added to Hindi Wikipedia.

We have identified three main forms of resources for new
topics,
1. News articles for current, relevant topics
2. Topics that are related to pre-existing Wikipedia pages and
3. Topics that are relevant in a particular field.

Named entity recognition is performed on each of these resources and
topics are extracted.

# Methodology

## Initial Proposed Methodology
The method initially proposed involved supervised learning based on vital topics that need to be present in every language.
In this approach, these topics are used as positive samples and new topics are classified. However, further analysis suggested that this might not be a good method, primarily because, topics that fall outside the scope of these vital articles but are still relevant (e.g. trending news articles) would not be included. Additionally, there is nothing such as a ’good’ or ’bad’ topic, especially when Wikipedia aims to encompass as much content as it can.

## Current Methodology
The current methodology is based on the collection of various types of useful resources and selection of possible topics after performing named entity recognition on the content.

![Flow Chart](/assets/Flowchart.png)

First, resources (news, domain articles,
wikipedia articles) are scraped for content. Then NER is performed on the content. Finally, possible new topics are identified from the list of named entities.

The primary focus of our current methodology is on collection of a wide variety of resources that are relevant in the Indian context and could contain probable new topics. We have identified three primary types of resources that collectively help in improving the breadth, depth and inter-connectivity of Wikipedia:

### Pre-existing Wikipedia articles
Wikipedia articles contain a lot of information about a specific article. This information can be extracted and analyzed for new topics that don't already exist in Wikipedia pages. This would improve inter-connectivity of topics.

### News
Trending Hindi news articles is a useful resource for new topics. This could potentially give a list of currently important people, events etc. that are unlikely to have a Wikipedia page considering their very recent. Extraction of new topics from the news would improve the breadth of the existing Wikipedia.

![Flow Chart](/assets/Resources.png)
<!-- ### {Domain specific resources:} New topics can also be identified from domain specific blogs and articles. These domains could include health, technology, politics etc. Identification of topics from such domains would improve the depth of the existing Wikipedia. -->

#### Header 4

*   This is an unordered list following a header.
*   This is an unordered list following a header.
*   This is an unordered list following a header.

##### Header 5

1.  This is an ordered list following a header.
2.  This is an ordered list following a header.
3.  This is an ordered list following a header.

###### Header 6

| head1        | head two          | three |
|:-------------|:------------------|:------|
| ok           | good swedish fish | nice  |
| out of stock | good and plenty   | nice  |
| ok           | good `oreos`      | hmm   |
| ok           | good `zoute` drop | yumm  |

### There's a horizontal rule below this.

* * *

### Here is an unordered list:

*   Item foo
*   Item bar
*   Item baz
*   Item zip

### And an ordered list:

1.  Item one
1.  Item two
1.  Item three
1.  Item four

### And a nested list:

- level 1 item
  - level 2 item
  - level 2 item
    - level 3 item
    - level 3 item
- level 1 item
  - level 2 item
  - level 2 item
  - level 2 item
- level 1 item
  - level 2 item
  - level 2 item
- level 1 item

### Small image

![Octocat](https://github.githubassets.com/images/icons/emoji/octocat.png)

### Large image

![Branching](https://guides.github.com/activities/hello-world/branching.png)


### Definition lists can be used with HTML syntax.

<dl>
<dt>Name</dt>
<dd>Godzilla</dd>
<dt>Born</dt>
<dd>1952</dd>
<dt>Birthplace</dt>
<dd>Japan</dd>
<dt>Color</dt>
<dd>Green</dd>
</dl>

```
Long, single-line code blocks should not wrap. They should horizontally scroll if they are too long. This line should be long enough to demonstrate this.
```

```
The final element.
```
