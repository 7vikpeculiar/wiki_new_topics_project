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
## Implementation Details
### Improving inter-connectivity using existing Wikipedia pages
Inter-connectivity of topics can be improved by adding more link enriching topics. Each of the Wikipedia articles can be viewed as a set of links to other Wikipedia articles. Since Hindi Wikipedia is only 1/10th the size of English Wikipedia, we hypothesize that a lot of topics can be found by filtering relevant words from pre-existing Wikipedia articles.
Around a thousand randomly chosen HindiWikipedia articles were scraped.
New topics extracted from these articles are related to the current topic and hence can be potential candidates for new topics if they aren’t already part of Hindi Wikipedia. This would help readers get information on related topics as the inter-connectivity of topics is better

On scraping the articles, it was observed that individual articles that
aren’t already present in Hindi Wikipedia are not very well-developed. A lot of important details are either missing or incomplete. Most of the articles were therefore quite small, or they didn’t contain too many new keywords.

![Flow Chart](/assets/Articles.png)

### Improving breadth of topics using news articles
A primary resource that would help identify topics of emerging interest and trending topics is news. Popular news articles ca be scraped and keywords can be extracted from them.

BBC Hindi news was scrapped for this purpose. BBC news is separated into various categories such as sports, entertainment, international, science, social and India. This made it easier to scrape as compared to other news websites. First, the homepage was scraped for articles from each category and new links were obtained by following recommendations from each page. Around 14,000 articles were scraped this way. The scraped data is present [here](https://iiitaphyd-my.sharepoint.com/:f:/g/personal/sathviksanjeev_b_research_iiit_ac_in/EqYL0iNQzFdAiclzs9uN474BZHlJa8NXPOW1h4_UdATwpQ?e=AT7xGg).

Extraction of keywords from news articles would help identify completely new events, thereby helping improve the overall breadth of Hindi Wikipedia.

![Flow Chart](/assets/Expansion.png)

### Improving depth of topics using domain specific articles}
Depth of Hindi Wikipedia articles can be improved by using domain specific articles. For example, by scraping articles relating to medicine and extracting corresponding keywords, we can improve the depth of the health domain.

Wikipedia already has a pre-defined taxonomy and this was used as a basis for vertical expansion of Hindi encyclopedia. Articles belonging to various domains like health, movies, politics, science, sports and technology were scraped from different blogs and websites that are relevant to the specific domain. The scraped data is present [here](https://github.com/SanjanaSunil/ire-major-project/tree/master/data).

#### Link to Video
<iframe width="560" height="315" src="https://www.youtube.com/embed/I7A8KhLrG1o" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
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
