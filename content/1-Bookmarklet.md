---
title: UI Login Bookmarklet
nav: true
---

# UI Login Bookmarklet

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
Created by the University of Idaho Library.  Get the bookmarklet [here](https://www.lib.uidaho.edu/find/articles.html#tools).

<a id="whatisit"></a>

#### What is it?

The log-in bookmarklet allows you to <a href="{{ '/content/0-Concepts.html' | relative_url }}">authenticate</a> through the UI from wherever you are on the internet without leaving that page.

<a id="value"></a>

#### Why would you use it?

About 70% of academic journal literature is estimated to be subscription-only \([Piwowar, 2018](https://peerj.com/articles/4375/)\).  For the UI community, the UI Library subscribes to a large part of this literature.  However, to gain access, the website where the article is located must recognize your affiliation with the UI.  The bookmark lets you do this with a single click, followed by your usual login method.

<a id="howitworks"></a>

#### How does it work?

When you click the bookmark, the browser is instructed to take your current url, such as  
```https://wildlife.onlinelibrary.wiley.com/doi/full/10.1002/jwmg.72```
and prepends the UI Library authentication url to it.  Then it reloads the page.  In order to proceed, the browser will ask you to log in.  When you do, a temporary cookie is stored on your machine that tells websites that you are affiliated with the University of Idaho.  In the case of journal articles, if we subscribe, you get access.

{% capture text %}
**Remember!** You cannot authenticate for websites that have nothing to do with academic literature.  So, if you try it using something that has nothing to do with the UI Library, such as ESPN.com, you’ll just get an error.
{% endcapture %}
{% include alert.md text=text %}

At a more general level, bookmarklets work by passing some browser-readable content into the browser’s queue.  Typically, when you create a bookmark, you just save a URL and on accessing it, you reload the page to that url (and/or create a new tab, etc.)  However, you can rewrite the bookmark content to run a javascript action instead.  In this case, we re-route the same url through the authentication system (UI Library's proxy server):
```javascript:void(location.href=%22http://ida.lib.uidaho.edu:2048/login?url=%22+location.href)```

<a id="howtouseit"></a>

#### How Do You Use it?

It's very simple!

1. Go to the UI Off-Campus Access Page
2. Drag the link to your bookmarks
3. Click whenever you want to authenticate

<a id="privacy"></a>

#### Privacy Concerns

There are no unique privacy concerns beyond the use of cookies for authentication, which occurs every time one logs in to use VandalWeb, Web Mail, or any other University of Idaho service.  The UI Library collects no data from this process.

<a id="limitations"></a>

#### Limitations

1. The first limitation is obvious.  The Library must subscribe to the journal!  If not, then it won’t work.  The bookmark does not make things available that otherwise would not be. 
2. The second limitation is that it only works for items that we have registered in our system.  For…reasons…, there may be a domain or two that we subscribe to, but that we have failed to register in our authentication system.  If you receive an error, this may be the case.


{% endcapture %}
{% include card.md text=text header="Summary" %}