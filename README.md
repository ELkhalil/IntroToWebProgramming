Introduction To Web Programming

1 - Back to Basics:
  _> What technologies RUN in a browser ?
    HTML - CSS - JAVASCRIPT
    - that's it! everything else is a variation on this.
  _> HTML
    HyperText Markup Language
    identifies elements of the web page:
    Header  Paragraph
    Footer  List
    Article  Links
    Section  Images
    Aside    Headings
    it does not dictate how the page looks!
  
  _> CSS
    Cascading Style Sheets
    Dictates how the page looks:
      Colors  Fonts 
      Spacing   Layout ...
    if it's pretty, it's probably CSS!
  
  _> JAVASCRIPT
    Dictates how the page interacts:
    Things that move.
    Things that change color.
    Things that change size. 
    Things that appear or disappear.
    Calculations
    if it's "interactive", it's probably JavaScript!
  
  BUT WHAT ABOUT:
    Bootstrap: HTML, CSS, JAVASCRIPT
    Responsive Design: HTML, CSS
    Wordpress: HTML, CSS, JS, and a database server.
    jQuery, React, Angulat, Vue: Javascript

2 - HTML (HyperText Markup Language)
-------------------------------------
  HTML's base building block is the tag. A tag is a building block. It describes what's inside it. Every tag has an 
  opening and a closing tag (some tags open and close at the same point.) I think the easiest way to learn it is just to show a bunch of examples.

  <h1>This is the title to my document</h1>
  This is the title to my document
  You can see the <h1> and the </h1> surrounding the the text "This is the the title to my document". 
  This is how HTML operates. You can have opening tag which has information or more tags inside of it. 
  In this case we have an h1 tag which is a heading tag: it's used for the biggest title on the page, 
  typically a title. If you rendered that using the browser

  HTML tag Breakdown:
    every tag consist of the following elements suppose the following example:
      <a  href="index.html" >  Home Page </a>
      breakdown:
        opening Tag consist of:
          <a> _> tag Name
          href="index.html" _> attribute witch consist of key=value pairs
        Enclosed Tag Content:
          Home Page
        closing tag:
        </a>
    Explaining the intro : <!DOCTYPE html>
        _> at the top of each document.
        _> force the browser to follow specifications.
        _> Prevent "quirk mode" when rendering.
          what is this quirk mode:
            _> to explain it we must go to the DOCTYPE History of Incompatibility
              The history of DOCTYPE incompatibility stems from the early web when browsers had varied interpretations of HTML and CSS. The "Browser Wars" in the late 1990s exacerbated the issue. DOCTYPEs were introduced to standardize, but challenges persisted. Efforts by organizations like W3C and the development of HTML5 aimed to improve consistency, but achieving perfect cross-browser compatibility remains a challenge, necessitating techniques like feature detection and polyfills for a consistent user experience.
    Explaining the html tag:
      _> the root element of an HTML document.
      _> All element must be descendant on <html>
      _> only one head per html
      _> no parent for this tag.
      _> only one body per html.
      ---> attribtes:
        Global attributes:
          class id lang dir .... there is a lot moral of the story is that this html tag accept all the global attributes
        Other
          manifest version xmlns
      ---> metadata:
        they are infos about the data... any kind of data an img for example has some metadata that has all the infos about it
        so every kind of data has at some point some metadata that holds informations about it
        in our main topis :
          HTML document is the data.
          the browser need some informations about this document to process it.
          metadata has the title ....and some other staff inside the head tag.
    Explaining he Head tag:
      _> contains the machine-readable informations metadata about the content
      _> permited content <meta> <title>
         the following are external staff: <base> <style> <link> <script>
  QUICK NOTES:
    _> when dealing with <h1> <h6> heading tags we must see them as an order of importance and not of size. size does not matter..
      - create content hierarchy.
      - structure the content.
      - Size defines importance.
      - try to have <h1> per document.
      - using heading tags to change the size. (don't)
      - don't not skeep levels.
    analyse headings of a website using the following extension:
      https://chromewebstore.google.com/detail/headingsmap/flbjommegcjonpdmenkdiocclhjacmbi?hl=en-US&utm_source=ext_sidebar
    to be good at picking the headings try to analyse the importance you have.
  PARAGRAPHS:
  ------------
  _> When your dealing with <p> the use of <br/>
    - insert line breaks in text
    - use it for address
    - use it for poetry
      (don't) use it for the styling please !!!
      it is communly used when putting an adress or a poem.
  _> Strengthen Text (strong) <strong></strong>
      we use it inside a pragraph when we need to:
        draw attention strong importance urgency seriousness
  _> Emphasize Text (em) <em>
      to add some stress Emphasis
  _> HTML "strong" vs "b" tags <b></b>
    they do the same thing they render the text span in bold, but the dirrefence is how the browser sees it:
      - in case of strong it takes it as a very important ..
      - in case of <b> he look at it as style dirrerence in text.
  HTML Entities:
  ---------------
    Character entities | entity codes
    -> display HTML reserved characters
    -> characters don't appear in the keyboard.
    for example:
      < less than 
      > grater than
    for example i want to display this an an html code:
      <h1> example of an h1 </h1>
      i want the tags to be displayed to do this we must add the following tag.
      google w3school to see the characters entities.
      exxample: <p>the price is 15 &euro;</p>
  Non-Breaking Space &nbsp;
    _> use it in case of two words to tell the browser to keep the word always joined like this 10&nbspkg
      use it in case if the user zooomed the website it will be splitted to prevent that from happening we use it.
    
  #1 img Element:
  ---------------
    it is a self closing tag
    <img src="path to image" alt="landscape" />
      src: required
           contains the path to the image.
      alt: not required
          contains description of the image.
          but it is very usedule for SEO && for people who are blind or have a disability
  #4 Problem: Dimensions & Resolutions
  -------------------------------------
    those are also solutions but it is not recommended to use them
    -> CSS media queries
    -> javascript
    -> server side
    use this instead:
      srcset="url size, url size, url size, url size"
      size:
        - width or density
      but we still add the src attribute as a fallback for the browsers that does not support srcset attribute.
  
  #1 Lists introductions and Examples:
  -------------------------------------
  Used in multiple use cases:
    - Accordion
    - Footer Elements
    - product list page.
    - navigations and nav bar for example.
  1 - Unordered lists:
    _> order does not mattaer
      <ul>
        <li>First Element</li>
        <li>Second Element</li>
        <li>Third Element</li>
      </ul>
  2 - Ordered lists:
    _> order does mattaer
      <ol>
        <li>step 1</li>
        <li>step 2</li>
        <li>step 3</li>
      </ol>
      attributes:
        1 - reversed: boolean to reverse the order.
        2 - start: Integer to start the counting from a number.
        3 - type: "a" to change the numbers to alphabet. or "A".
  3 - Description lists:
    to group some informations about one single item
    _> list of groups of terms
      <dl>
        <dt>Authors</dt> dt: stands for definition term
        <dd>abdo</dd> dd: stands for definition description
        <dd>rachid</dd>
        <dt>editors</dt>
        <dt>abdoul</dt>
      </dl>
  #1 Hypertext and Hyperlinks:
  ------------------------------
  Hypertext: is a tet which contains links to other texts.
    normal text -> linear
    hypertext -> non-linear
  Hyperlink: is a type of content that you can click on to jump to a new document.
    # Anchor Element (a) Breakdown (anchor tag)
     <a href="index.html" title="target page title"> Home Page </a>
    href: stands for hypertext reference it can have URL/Address as value.
    title: good for SEO and for accessibility.

  #1 Tabular Data Introduction:
  ------------------------------
    every table consist of the following a row, column and a cell
    <table> : telling the browser it is a table
    <th> : table header: it is the header of a group of table cells
    <tr> : row of cells (table row)
    <td> : table data cell

  #1 Content (Tags) Categories Introduction:
  -------------------------------------------
    check the venn diagram to simplify this
  Metadata content:
  Flow content
  Sectioning content
  heading content
  phasing content
  embedded content
  interavtive content:
  other:
    <!doctype html> <html> <head> <body>
  -> Analyze a Design for Categories Elements introduction
    we will focus on 4 major ones: 
      1 - Sectioning content to analyse layout of the design. (header section footer...)
      2 - heading content to analyse headings in our design.
      3 - Embedded content to analyse external recources.
      4 - interactive content when the user manipulate something.
  #6 Thinking Style Vs. Thinking Semantic to write HTML Code
  -----------------------------------------------------------
  when decompiling a design try to see the value of it that's the semantic view and not to try to see the sizes
  try to develop a semantic view the importance take the big part and ...
  HTML MUST BE SEMANTIC to take care of your SEO and also for the screen reader for people who can have a disability.
    what's the tag that will best describe this part ? is it good for my SEO ? and also for screen readers ?
  Semantic Tags Examples:
    <abbr>: for abbreviation
    <blackquote>: long quotation
    <dfn>: definition
    <address>: address for author(s) of the document.
    <cite>: citation
    <code>: code reference.
    <h1>: first-level headline
    <h2>: second-level headline
    <h3>: third-level headline
    <h3>: fourth-level headline
    google more...
  #1 Navigation Element Introduction and Use Cases
   -----------------------------------------------
    navigation links point to:
      current document
      external document
    Extra structure
    semantic markup
    help screen readers
    When to use it:
      - menus
      - tables of content
      - pagination (pages break down)
      - breadcrumb (category and it's parent link...)
  #8 Generic Section Element (section) Introduction:
  --------------------------------------------------
  try to group your elements with a section tag if it does not have a groping tag
  like : articles section, products section, hero section, gallery section...etc
  - structural HTML element
  - if an element doesnt have a semantic tag to represent it.
  - group related elements
  - each section includes x1 or n headings
  - shouldn't be used as a generic container
    !!!most people uses div in everything we use div to devide an element for example if we are inside a hero section and 
      we want to devide it into multiple group we ucan use a div to do that inside a section.
  #10 Aside Element (aside) Introduction
  --------------------------------------
  <aside> defines a section that is tangentially (relates slightly to a matter) related to the content around it.
  Content that is associated with the main content of the webpage BUT does not form the primary content of the page.
  Pull Quotes, Sidebars, Advertising, Additional Information, Blogroll.
  1 - Pull Quotes
  2 - Comments
  3 - Advertising
  #22 Content Division (div) Element
  ------------------------------------
  use it as a generic tag but only when there is no semantic tag to use.
  devide & group to make the styling easier.

  #1 What are Web Forms & Sending Form Data Basic Architecture:
  -------------------------------------------------------------
  the form is just a user friendly interface to sen an http request to the server containing some data.
  it does this:
    Configure HTTP-REQUEST   -----------(FORM)----------->  Send HTTP_REQUEST to the server
  it has an action:
  <form action="">
    defines where (Server) the data gets sent
    value: Valid Absolute URL
  
  /*
    use ids to link elements and keep the style to using classes only.
  */

2 - CSS (Cascading Style Sheets)
---------------------------------
    as we finished talking about HTML witch is the structure and the base of our website pages we are now ready to 
    take care of the view of our pages.
    CSS take care of the following:
      it consist of the 
        Layout: laying out elements in a pre defined and ruled way
        fonts: upload the fonts and take case of the texts
        colors of course to bring life to the page.
    - presentation of a page
    - differente devices adaption
    - independent from HTML
    - ease of maintanability: once there us an issue you can easily identify it by checking if it is from presentation or structure
    - structure separation
  # to disable a design from a page to check it's structure use:
    https://chromewebstore.google.com/detail/web-developer/bfbameneiokkgbdmiekhjnmfkcnldhhm?hl=fr
  #5 CSS Snapshots & Modules
  -----------------------------
  CSS Snapshots and CSS Modules are terms related to web development:
    1. **CSS Snapshots:** There isn't a widely recognized term "CSS Snapshots" in the context of web development.
    It's possible you may be referring to capturing or saving a snapshot of the current state of CSS styles in a particular moment.
    2. **CSS Modules:** CSS Modules refer to a modular approach in web development where styles are scoped locally to a component or module.
    This helps in avoiding global style conflicts and enhances code maintainability. It involves techniques like scoped CSS and local identifiers.
  #8 CSS Standardization - Which Module to use in your Code Base?
  ----------------------------------------------------------------
  WD: Working Drafc when you see a module with this state it means it is not stable.
  CR: Candidat Recommendation
  PR: proposed Recommendation
  REC: recommendation
  |------------------------------------------------------------------------------------------------|
  | i loved the content shared by a youtube channel:                                               |
  |   https://www.youtube.com/watch?v=SqNsT16yYpw&list=PLyMSoUmH8WzDaQBKdkO7tlOe8SU5_5dSA&index=10 |
  |     he uses:                                                                                   |
  |       - Screen Recording: Screenflow                                                           |     
  |       - Writing on the screen: Screen Brush                                                    |
  |       - Slides: Keynote                                                                        |
  |------------------------------------------------------------------------------------------------|











