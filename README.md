#Kiwi Wiki

Kiwi is a light-weight [Wiki markup
language](http://c2.com/cgi/wiki?WikiMarkupLanguage).  It is intended to be
*simple*, *elegant* and *intuitive*.

##1. Motivation

Every Wiki markup language in use today sucks!  Their syntax is *neither*
elegant *nor* intuitive.  Kiwi means to remedy this.

##2. Kiwi Syntax

The syntax is inspired by both the [Creole
1.0](http://www.wikicreole.org/wiki/Creole1.0) Wiki standard and the [txt2tag
source format](http://txt2tags.org/manpage.html#markup).  It is not fixed yet.
Here is part of it.

###2.1. Kiwi Headings (Till Level 6)

The syntax for unordered and ordered headings matches that for unordered and
ordered lists.  The former defines *larger* document structures, so `=` and
`#` are used respectively; the latter defines smaller block structures, so `-`
and `+` are used respectively.

For a heading to be recognized, it must be surrounded by (at least) two empty
lines except that it appears in the first line of the file, in which case,
only one empty line (or more) is required.

####2.1.1. Kiwi Unordered Headings

```
=Unordered Heading 1
```

#Unordered Heading 1

```
==Unordered Heading 2
```

##Unordered Heading 2

```
===Unordered Heading 3
```

###Unordered Heading 3

####2.1.2. Kiwi Ordered Headings

```
#Ordered Heading 1
```

#1. Ordered Heading 1

```
##Ordered Heading 2
```

##1.1. Ordered Heading 2

```
###Ordered Heading 3
```

###1.1.1. Ordered Heading 3

###2.2. Kiwi Lists

Refer to the remarks on the syntax for headings.

####2.2.1. Kiwi Unordered Lists

```
- Red
-- Green
--- Blue
```

* Red
   * Green
      * Blue

####2.2.2. Kiwi Ordered Lists

```
+ Red
++ Green
+++ Blue
```

1. Red
   1. Green
      1. blue

####2.2.3. Kiwi Definition Lists

```
Red
: a color
Green
: a color
Blue
: a color
```
in HTML

```
<dl>
 <dt>Red</dt>
 <dd>a color</dd>
 <dt>Green</dt>
 <dd>a color</dd>
 <dt>Blue</dt>
 <dd>a color</dd>
</dl>
```

###2.3. Kiwi Paragraph

```
A paragraph consists of one or more lines.

A blank line ends a paragraph.
```

A paragraph consists of one or more lines.

A blank line ends a paragraph.

###2.4. Kiwi Code Block

The simple requirement is that the symbols chosen should remind of code.
Braces are probably the most-used symbols in code.

```
{
code block
}
```

```
code block
```

Symbols like <tt>```</tt> or <tt>'''</tt> are not chosen as they sit too much
high above the baseline, which makes it hard for the eyes to isolate them from
adjacent lines.  Compare the following syntax chosen by Markdown with the above
syntax:

    ```
    code block
    ```

By default, a code block is indented one column to the right.  To indent more
columns, use more braces.  For example, `{{` and `}}` will indent the code
block two columns to the right.

###2.5. Kiwi Text

The markup syntax for font faces all use *linear* symbols.  These symbols
should as much as possible suggest the look the surrounded text will get after
formatting.

####2.5.1. Kiwi Bold Text

```
|bold text|
```

**bold text**

####2.5.2. Kiwi Emphasized Text

```
/emphasized text/
```

*emphasized text*

####2.5.3. Kiwi Underlined Text

```
_underlined text_
```

in HTML

```
<u>underlined text</u>
```

####2.5.4. Kiwi Strikethrough Text

```
-strikeout text-
```

in HTML

```
<strike>strikeout text</strike>
```

When using strikeouts, it is recommended leaving at least one space at both
the begining and the end, because hyphen `-` is usually used to form a
compound word.  Text like the following should not be formatted as strikeout.

```
A compound-word is not a pseudo-word.
```

But the text as follows should.

```
A compound -word is not a pseudo- word.
```

####2.5.5. Kiwi Inline Code

For inline code, since it is smaller, their markup syntax better only differs
from that for a code block on *weight*.  Hence the same symbols are used but
they are *lighter*.

```
{code piece} in text
```

`code piece` in text

###2.6. Kiwi Horizontal Rules

The number of `~` does not matter.  But they exclusively occupy a line.

```
~
```

----

