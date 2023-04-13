HtmlCleaner
=================================================

![Points](../../blob/badges/points.svg)

For this homework, you will "clean" HTML leaving only the text content. This includes converting or removing HTML entities, removing HTML tags and comments, and removing some HTML block elements.

#### Handling Entities ####

[HTML entities](https://developer.mozilla.org/en-US/docs/Glossary/Entity) are how special characters are encoded in HTML. For example, the entity `&copy;` renders as &copy; in HTML and is the `©` Unicode character.

Each HTML entity should be converted from the HTML representation to its Unicode character when possible using the [StringEscapeUtils.unescapeHtml4](https://commons.apache.org/proper/commons-text/javadocs/api-release/org/apache/commons/text/StringEscapeUtils.html#unescapeHtml4(java.lang.String)) method of the [Apache Commons Text](https://commons.apache.org/proper/commons-text/) third-party library. 

Any entities that cannot be converted must be removed. (This includes some valid HTML 5 entities, as those are not yet supported in this library.)

## Hints ##

Below are some hints that may help with this homework assignment:

  - View the Javadoc comments using the "Javadoc" view in Eclipse. It will render the HTML in the comments properly.

  - Each method can be completed using a combination of regular expressions and the [String.replaceAll](https://www.cs.usfca.edu/~cs212/javadoc/api/java.base/java/lang/String.html#replaceAll(java.lang.String,java.lang.String)) method.

  - You will have to generate a regular expression for the `HtmlCleaner.stripElement` method based on the element name provided as a parameter. It can be helpful to use Java [format strings](https://www.cs.usfca.edu/~cs212/javadoc/api/java.base/java/util/Formatter.html) for this, but it is not required.

  - If you are getting stack overflow exceptions, it is likely your regular expressions are too complicated or too greedy. Try to simplify and reduce the number of greedy quantifiers used.

These hints are *optional*. There may be multiple approaches to solving this homework.

*Note:* Before using these classes with project 4, you will need to make some modifications. Specifically, you will eventually need to make your `LinkParser`, `HtmlCleaner`, and `HtmlFetcher` work together so that you fetch HTML, then parse links after stripping block elements, but before stripping tags and entities. (This is not required for the homework, however.)

## Instructions ##

Use the "Tasks" view in Eclipse to find the `TODO` comments for what need to be implemented and the "Javadoc" view to see additional details.

The tests are provided in the `src/test/` directory; do not modify any of the files in that directory. Check the run details on GitHub Actions for how many points each test group is worth. 

See the [Homework Guides](https://usf-cs272-spring2023.github.io/guides/homework/) for additional details on homework requirements and submission.