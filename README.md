README — Roc Intermediate Guide: Extracted Code Blocks

This folder contains every code snippet pulled from Roc Intermediate Guide, organized by chapter and kept in the order they appear.

What’s inside
roc_codes_by_chapter/
  README.txt
  chapter-01_Title-or-topic/
    code-01.roc
    code-02.roc
    ...
  chapter-02_...
  ...


Chapters detected: 16

Code blocks extracted: 210

Total lines of code: 492

File naming: chapter-XX_ShortTitle/code-YY.roc

Extensions are .roc by default. You can rename them if you prefer another suffix.

How these files were created

The original .docx was parsed and scanned paragraph by paragraph.

A simple set of rules flagged “code-like” lines, for example:

Typical code tokens such as import, def, let, match, ->, ::

Indentation with multiple leading spaces

Lines with many brackets and symbols

Consecutive code-like paragraphs were grouped into a single block.

Chapters were detected from headings that look like Chapter 3, and the next non-empty line was used as the chapter title.

How to use this set

Browse by chapter: Open the folder for the chapter you are working on and read the block files in order.

Run or test: Change .roc to the extension your toolchain expects if needed.

Search quickly: Use your editor’s global search to find a function, type, or keyword across all chapters.

Suggested workflows

Merge per chapter: Concatenate all code-*.roc files inside a chapter into one file if you want a single runnable example per chapter.
Example on macOS or Linux:

cat chapter-03_YourTitle/code-*.roc > chapter-03_YourTitle/all-examples.roc


Change extensions:

# Example: convert .roc to .txt
for f in chapter-*/code-*.roc; do mv "$f" "${f%.roc}.txt"; done

Quality checks you can do

** Spot-check a few chapters:** Open the book and confirm the first and last snippets in a given chapter match the extracted files.

Check order: The numbering code-01, code-02, etc., reflects the order in the book.

Look for false positives: Rarely, a paragraph with many symbols might be picked up as code. If a block looks like prose, you can delete it or move it out.

Known limitations

Heuristics: Detection is based on simple rules. It captures almost all code, but very short one-line examples or inline code in sentences may be skipped.

Chapter titles: The folder’s short title is taken from the first non-empty line after a “Chapter X” heading. If a chapter has an unusual structure, the title may be generic.

Formatting: Original inline formatting from the book is not preserved. These are plain text files.

Customization

If you want me to:

merge all blocks into a single file per chapter,

switch all file extensions,

split large blocks by subheadings,

or export a CSV index of snippets by chapter,
