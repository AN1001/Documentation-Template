### Documentation Template
Working demo: https://adb-docs.pages.dev/

![UI](https://github.com/user-attachments/assets/1ac82e61-2ad9-4221-8fae-7e07b6d60fbc)
This is a template for documentation of any kind.

Provides only basic support for simple documentation, some features include:
  - Title
  - Text with inline spans
  - Support for Bold, Italics and Code
  - Code area (no syntax highlighting)
  - Blockquote
  - Blank space
  - Links
  - Pictures

- .sfl format is structured format language
- Just add a section and link a .sfl file to make a new page

### .sfl files
A structured format language file will look like this
```text
<title>This is an SFL file
<text>Here is some text explaining
how an sfl file works
new lines don't make a difference and this will
all be compiled as one line

Two lines will make a difference and make this text a new paragraph


Three lines will make this a new paragraph with a space between the two, in
essence making each blank line a \n character, 
~
~
and each tilda is used only as a filler character to make the file clearer,
they will be treated as if they don't exist
~
<code>const some_code = "code";

// Each new line of code needs a blank space between them

function new_doc(){

// TODO

}
```

### Sections.js
Make sure you edit the sections.js file to include your pages
```javascript
const setup_section = {
    header:"Setup Code",
    subsections:["Dependancies", "Quick Setups", "Examples"],
    subsection_file_names:["dependencies.sfl","qs.sfl","examples.sfl"]
}

const demo_section = {
    header:"Demo Code",
    subsections:["Todo List", "Ticker"],
    subsection_file_names:["todo.sfl","ticker.sfl"]
}

const contents = [setup_section, demo_section];
export default contents;
```

This will create two major sections with subsections:
- Setup Code
    - Dependencies
    - Quick Setups
    - Examples
- Demo Code
    - Todo List
    - Ticker
 
  
