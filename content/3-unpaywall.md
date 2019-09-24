---
title: Unpaywall
nav: true
---

# Unpaywall

In this section, we'll describe the Unpaywall service from OurResearch. We will primarily discuss the browser extension, but other uses of Unpaywall are possible, such as API access to the database.

**What you'll find on this page:**
- <a href="#source">Source</a>
- <a href="#whatisit">What is it?</a>
- <a href="#value">Why would you use it?</a>
- <a href="#howitworks">How does it work?</a>
- <a href="#howtouseit">How to use it</a>
- <a href="#privacy">Privacy Considerations</a>
- <a href="#limitations">Limitations</a>

{% capture text %}
<a id="source"></a>

#### Source
[Our Research](https://ourresearch.org), a 501(c)3 nonprofit organization based in Vancouver, B.C.  They have a number of related projects in the open science (def) domain, including Unpaywall, GetTheResearch, and Impactstory Profiles.
Get the browser extension [here](https://unpaywall.org/products/extension).

<a id="whatisit"></a>

#### What is it?

Unpaywall is an index and database of nearly 25 million free scholarly articles.  The database maintains descriptions of the accessibility of the journal, of the article, of the nature of access [link to types], and more.  They crawl tens of thousands of hosting locations, including institutional and disciplinary repositories, academic journal websites, and more.

<a id="value"></a>

#### Why would you use it?

Approximately 25-30% of the academic literature is open access.  This means that at least of quarter of all scholarship shouldn’t require a subscription.  However, publishers do not always link to available open versions, or the information about those versions do not travel through the various indices, catalogs, and so on.  In those cases, the Unpaywall extension will give you an indicator of whether or not there is an alternate copy available.

<a id="howitworks"></a>

#### How does it work?

The browser extension is built in Javascript \([see the code here](https://github.com/Impactstory/unpaywall)\). It scrapes the entirety of each page you visit while active, and looks for a pattern that looks like a DOI or DOI link {def}. When it finds something DOI like, it sends that to Unpaywall’s [API](https://unpaywall.org/products/api) to find the article and retrieve the relevant information. Once it obtains that, it will display the relevant icon that indicates whether or not there is a copy and the color of the type of access available.

In other words, you browse around as you would, and if you are on a page with a DOI, the extension will light up (or not) depending on whether or not you can get a copy of an article.

<a id="howtouseit"></a>

#### How Do You Use it?

*Installation:*<br>
First, install the extension.  Once there, it lives in your browser and works behind the scenes.

*Use:*<br>
You click on the icon when you see it indicating that there is an available copy.  Otherwise, you don’t.  Easy!

*Settings:*<br>
Change things.  Maybe provide list of acceptable domains?

<a id="privacy"></a>

#### Privacy Concerns

According to Unpaywall, they do not collect any personally identifiable information (PII) (def) when you use the browser extension. The extension also does not use beacons, cookies, or similar technologies. However, when you use their other services, there may be other transmissions of PII. They do collect some non-personal information – IP addresses, anonymous usage data, referring pages/URLs, browser, language used, date/time of requests made.  You may or may not agree that this is not PII; there is some disagreement about whether or not IP addresses are personal or non-personal information. [link] 
View their privacy policy [here](https://unpaywall.org/legal/privacy).

<a id="limitations"></a>

#### Limitations

The extension only works for open access content (or DOIs?).  If there is no open version, there will not be a link available.  It is also limited by what Unpaywall has indexed.  There may be open content that they have yet to discover and index, or that they missed.  At 25 million items, that’s probably not a common problem, but it is possible.

{% endcapture %}
{% include card.md text=text header="Summary" %}