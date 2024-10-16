# MA-redirect

A browser extension that allows you to hop over the metal-archives.com search
page.

## Use case

If you're anything like the average person, you're on MA several times a day and
use the search functionality extensively, whether through the main page, or with
a browser search shortcut. Many bands (albums, etc.) have the same name, of
course, and often one just wants to go see the page of the most popular band
with the given name. This script allows that to happen.

(Background: I first remember wishing for something like this script about seven
years ago.)

## What does it do?

The URL parameters are parsed and used to look up values in a dictionary. The
user is then redirected to the stored URL.

## How do I add my own redirects?

Simply edit the return value of `redirects()`. Watch out for commas, quoting,
etc. Note that the values are case sensitive.

If the script has stopped working after you've changed some values, but you
don't see any error messages in the JS console, paste the script into said
console. You'll then be informed of syntax errors. If all else fails, feel free
to send me a message, and I'll take a look at it.

## Note on updates

This script is fairly trivial, and I don't foresee there being any updates. If
that were to happen, though, any customizations you've made will be lost.
Therefore I recommend turning off automatic updates. If you need to pull down an
update, be sure to save your customizations first. (Yes, a solution could be
made to store the redirect values, check versioning information, and
prompt/inform the user about potential conflicts, but I don't want to add that
functionality.)

## What if I want to see all the bands with "Death" in the name?

Simply append a `%` to the search string. (Many other non-alphabetic characters
will work as well.) Type the following into the search field (or using a browser
search shortcut):

> Death%

MA will disregard the `%` and you (presumably) won't have defined a redirect
with the key `Death%`, so you'll see the normal search results page.

Alternatively, you could have all your redirects use proper capitalization and
use lowercase characters for searching.

## Changelog

- 1.1: README to markdown on greasyfork.
- 1.2: Removed unnecessary information from README, minor wording fixes.
- 1.3: Update README.
