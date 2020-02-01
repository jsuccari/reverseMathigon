# reverseMathigon

## Course Structure

Every course consists of a few different components:

* `content.md` contains the source code and metadata for a course. It is
  written in a [custom extension](https://mathigon.io/markdown) of
  [Markdown](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet).
  
  
* `functions.ts` contains all course-specific TypeScript code.







* `styles.less` contains all course-specific styles, in
  [LESS](http://lesscss.org/) format.
  
* `hints.yaml` (optional) contains any messages that can be sent by Mathigon's
  virtual personal tutor.
* `concepts.yaml` (optional) contains parts of Mathigon's internal knowledge
  tree for this topic.

The [shared directory](content/shared) contains biographies, glossary and assets
used by multiple courses.

Biographies: Mathematicians
Glossary: Mathematical terms
Assets: 



Every course is divided into multiple steps, each with a unique ID. These IDs
are used as function names in `functions.ts` when exporting the setup code
for every section. Every function gets called with a `$step` argument, when
the corresponding step is revealed for the first time. Check
[types.d.ts](content/shared/types.d.ts) for the available properties and
methods.

The [server directory](server) contains a simplified version of Mathigon's web
server. It is used for local testing, but should not usually be modified.
