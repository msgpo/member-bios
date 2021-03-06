# Hack4Impact Member Bios

This repository contains basic information about Hack4Impact members that will
be displayed on the [organization website](http://hack4impact.org/team/)
(or will be soon!).

Feel free to open a pull request to update your information at any time, but
please do not commit to `master` or merge the request without approval.


## Instructions

### Member Text

Copy the template below into a new file `firstname-lastname.md`. Each member bio
is a Markdown file with a YAML header marked by `---`. The header contains some
metadata, and the document body should contain paragraphs about you.

#### Header fields

Template metadata:
- `layout`: **Don't change this.** This should always have the value `profile`.
  It's used internally by the site generator ([Jekyll](https://jekyllrb.com/))
  to render the Markdown file into a webpage.

Biographical info:
- `first_name`: Your first name.
- `last_name`: Your last name.
- `class_of`: Your (expected) graduating class.

Contact information (each of these fields are optional, so only include the ones
you want):
- `email`: An email address that can be used to contact you. Note that this
  address will be made public, so you may want to set up mail filters or use a
  different email than your primary one if you choose to include an email.
- `website`: The _URL_ of your personal website.
- `github`: Your GitHub _username_ (not URL).
- `twitter`: Your Twitter _handle_, without the leading `@`.
- `linkedin`: The _URL_ of your LinkedIn profile (their username conventions are
  somewhat inconsistent).

#### Exec board members

In addition to the fields listed above, exec board members should include the
following (note that `role` is indented):

```markdown
---
exec:
  role: External Relations Chair
---
```

#### Alumni

In addition to the fields listed above, organization alumni should include the
following:

```markdown
---
alum: true
---
```


#### Template

```markdown
---
layout: profile

first_name:
last_name:
class_of:

email:
website:
github:
twitter:
linkedin:
---

Add your bio here.

Note that you _can_ use standard **Markdown** formatting here. Please don't
include any headers or non-paragraph elements, however.
```

#### Example

Here's an example of the required formatting.

```markdown
---
layout: profile
first_name: Benjamin
last_name: Franklin
class_of: 1744
alum: true

email: benf@seas.upenn.edu
twitter: benfranklin
github: bfranklin
linkedin: https://linkedin.com/in/benjamin.franklin
---

Benjamin Franklin was one of the Founding Fathers of the United States. A
renowned polymath, Franklin was a leading author, printer, political theorist,
politician, freemason, postmaster, scientist, inventor, civic activist,
statesman, and diplomat. As a scientist, he was a major figure in the American
Enlightenment and the history of physics for his discoveries and theories
regarding electricity.
```

### Member Photo

Each member's photo should be named `firstname-lastname.jpg`. Additionally, each
photo should be square and resized to 600 x 600. This can be done on the command
line using ImageMagick:

```sh
$ brew install imagemagick
$ convert <firstname-lastname>.jpg -gravity center -resize 600x600^ -extent 600x600 <firstname-lastname>.jpg
```
