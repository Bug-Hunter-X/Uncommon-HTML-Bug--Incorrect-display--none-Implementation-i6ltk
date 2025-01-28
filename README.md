# Uncommon HTML Bug: Incorrect 'display: none' Implementation

This repository demonstrates a subtle bug related to setting the `display` style of an HTML element to `none` using JavaScript.  The incorrect approach, while seemingly functional, can lead to unexpected behavior when retrieving style attributes later.

## Bug Description
The `bug.html` file shows the problematic code.  Setting `document.getElementById("myDiv").style.display = "none"` doesn't correctly set the `display` attribute.  This means that subsequent attempts to retrieve the attribute might return `null` instead of `"none"`, causing unexpected behavior in more complex scripts.

## Solution
The correct approach, demonstrated in `bugSolution.html`, uses `document.getElementById("myDiv").style.setProperty("display", "none")`.  This method ensures the `display` attribute is properly set and available for retrieval later.

## How to Reproduce
1. Clone this repository.
2. Open `bug.html` and `bugSolution.html` in a web browser.
3. Inspect the behavior of the script in the browser's developer tools. Note the different outcomes.
