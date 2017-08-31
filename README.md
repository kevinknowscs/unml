# Unified Navigation Markup Language

Introduction
------------
This document is a draft proposal for a new XML-based markup language, named Unified Navigation Markup Language, or UNML. 
It's purpose is to provide a way to author the Table of Contents section of a knowledge base, such that a hosting platform 
can combine multiple knowledge bases independently authored and hosted in a single location, with a unified table of contents 
and search space.

Status of Submissions to Standards Bodies
-----------------------------------------
This document has currently not been submitted to any standards bodies for consideration as an official Internet standard, although
it is the author's desire to ultimately do such a thing. At the time of this writing, the author has no idea how to even begin
such a process.

Definitions
-----------
Knowledge base - This is a general term to refer to any self-contained, bounded set of documents. We would envision the primary type
of document to be HTML, but could include any well-recognized document format such as XML, PDF, JSON, etc. An example of a knowledge base would be the tutorial and reference documentation for an open source programming framework. A web site could also be considered
to be a knowledge base.

Links - The knowledge base documents can contain links to other pages, either pages within the knowledge base itself, or to pages
external to the knowledge base.

Inner Links - When a knowledge base hyperlink refers to a page within the bounded surface of the knowledge base it is considered an
inner link.

External Links - When a knowledge base hyperlink refers to a page outside of the bounded surface of the knowledge base, it is 
considered an external link.

Table of Contents - The Table of Contents of the knowledge base provides the overarching navigation of the content of the knowledge
base. It is ordered and hierarchical.

Problem Statement
-----------------
We address two specific problems with the current state of web document authorship.

First, the author knows of no existing standard for semantically authoring the Table of Contents of a knowledge base. Every web site
must provide some means of allowing the user to discover and navigate through pages of the site. This can be done in numerous ways,
either through static content, or dynamically generated content done in either the backend or frontend (typically using JavaScript).

If each page of the knowledge base provided the navigatable Table of Contents, either statically or dynamically, then it violated
the Don't Repeat Yourself (DRY) principle, a well-recognized software engineering principle.


