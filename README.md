# Docs.js

Docs.js makes code documentation easy and friendly. Comment your code using Markdown syntax and
docs.js will automagically generate beautiful docs in realtime. No tools to install, no convoluted build
process and integrating your docs into an existing site is a breeze.

## Usage:

1) Comment your source:

    /**
     *
     * I'm a Header
     * ============
     *
     * 1) And
     * 2) I'm
     * 3) A
     * 4) List
     *
     */

2) Include docs.js in the page where you'd like to display your docs markup:

    <script type="text/javascript" src="docs.js"></script>

3) Either call docs.js with a reference to the element where you'd like
   your docs markup to be displayed:

    <div id="docs"></div>

    <script type="text/javascript">
      new docs("your.js", document.getElementById("docs")).generate();
    </script>`

4) Or just place the script tag inside the target element and let 'er rip:

    <div id="docs">
      <script type="text/javascript">
        new docs("your.js").generate();
      </script>
    </div>

## Methods:

### Generate

Initiates fetching of source code and generation of docs.

> ### Parameters

>> None

> ### Returns

>> Nothing

### Fetch

Retrieves the document at the specified URL using a cross-platform AJAX call and returns
the contents to *callback*.

> ### Parameters

>> #### **url** (string)
>> The URL to be fetched.

>> #### **callback** (function)
>> The function to be called after a successful fetch. Content will be 
>> passed as the first parameter.

> ### Returns

>> Nothing

### Parse

Parses comments out of source code and runs them through Showdown to generate docs markup.

> ### Parameters

>> #### **data** (string)
>> The source code to be parsed.

> ### Returns

>> #### **String**
>> A string containing the generated markup.