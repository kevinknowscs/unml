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
We address two specific problems with the current state of knowledge base authorship.

First, the author knows of no existing standard for semantically authoring the Table of Contents of a knowledge base. Every knowledge
base (e.g., a web site) must provide some means of allowing the user to discover and navigate through pages of the site. This can be 
done in numerous ways, either through static content, or dynamically generated content done in either the backend or frontend 
(typically using JavaScript).

If each page of the knowledge base provides the navigatable Table of Contents, either statically or dynamically, then it violates
the Don't Repeat Yourself (DRY) principle, a well-recognized software engineering principle. Furthermore, since the Table of Contents
is mixed together with the regular content of the page, and there is no existing standard, it is impossible for a third-party 
program to query the content to discover the Table of Contents without human intervention. By creating a standard semantic language
for authoring Table of Contents, the author of the knowledge base can separate navigation and content, making the Table of Contents
queryable and discoverable.

This leads us to the second problem. We want to create a way for the Table of Contents of multiple knowledge bases be merged together
and presented with a unified Table of Contents by a hosting platform that is independent of any of the knowledge bases. Thus, a
knowledge base consumer that wishes to consume content from multiple knowledge bases can have a single place they can visit, and
be presented with a coherent, unified Table of Contents that spans all knowledge bases of interest, presumably with a consistent
look-and-feel.

We envision a UNML-compliant knowledge base hosting platform that can host multiple knowledge bases in a single location. As the
UNML standard is intended to eventually be an open standard, any organization wishing to create such a platform could do so without
any restrictions or licensing fees. Such a platform could be open source or commercial, cloud-based or locally installed, web-based
or written using a GUI framework, etc. We would hope that there would be many multiple and complementary implementations of the
UNML standard.

Likewise, we would hope that eventually UNML would be popular enough that organizations that publish knowledge bases would do so in a
UNML-compliant way. In particular, we would hope that producers of open source programming frameworks, libraries, tools, and 
components would publish their documentation in a UNML-compliant way.

Sample Workflow
---------------
1. The user creates an account on their preferred UNML-compliant knowledge base hosting platform. Their workspace appears empty at
first, because they have not yet added any knowledge bases. For this example, we will assume the user is a programmer working on
a software project that uses approximately a dozen open source libraries. This is very typical of a real-world software project.
2. The user is using React as the primary framework for their project. They want to add the React documentation to their workspace.
They click the "Add Knowledge Base ..." command and are prompted for the URL of the UNML for the knowledge base. They type
"http://reactjs.com/react.unml" and hit enter. Immediately afterwards, all of the React documentation appears in the navigation 
section of their workspace.
3. The user likewise enters the UNML addresses for the other technologies they use in their project: TypeScript, WebPack, NodeJS,
npm, IntelliJ, Griddle, .NET Core 2.0, LazyJS, etc. The navigation section of their workspace now contains a unified Table of 
Contents the encompasses all of the technologies they use on the project.
4. The user peruses the document at their leisure. With each session she discovers some wonderful nuances about the technology
she is using.
5. The user conducts a keywork search and finds all relevant documents in all of her knowledge bases.
6. After a year or so, the user moves onto a new project. The new project uses Angular instead of React as the primary web UI
framework. Thus she no longer cares about React and doesn't want the React documentation to clutter up her workspace. She simply
removes React from her workspace, and adds Angular. In this way, her workspace always contains everything she cares about, and
nothing she doesn't care about.

Current Examples of Similar Technologies
----------------------------------------
TODO

* Dash
* MSDN

UNML Adapters
-------------
As with any new technology, it may take some time for the standard to become widely adopted. Since we need both UNML producers
and consumers to create a viable, robust community, there is a chicken-and-egg adoption problem.

To solve this problem, we envision that motivated organizations that wish to spur the adoption of UNML could write adapters that
would transform non-UNML-compliant content into UNML-compliant content.
