# web-dev-starter

This is a starter project for web development with no frameworks and minimal
dependencies. It is intended to be a starting point for web development projects
that are written in plain HTML, CSS, and JavaScript.

## Getting Started

To get started, clone this repository and run the following commands:

```bash
npm install
```
This will install the necessary dependencies for the project.

## Development

It is recommended to use the VSCode Live Server extension to run the project
locally. This will allow you to see changes in real-time as you make them. There
is no need to run a build process or refresh the page manually. Additionally,
you do not need to setup a local server to run the project.

## Testing

To run the tests for the project, run the following command:

```bash
npm test
```

## Accessibility Lab Answers

## Color
    1. The text is difficult to read because of the current color scheme. Can you do a test of the current color contrast (text/background), report the results of the test, and then fix it by changing the assigned colors?
    
    - I tested the contract and saw that drk text on neon green or dark green failed. after switching to white backgrounds with a dark text, everything became much easier to read.

## Semantic HTML
    1. The content is still not very accessible — report on what happens when you try to navigate it using a keyboard.

    - When trying to navigate using the keyboard the site is kinda accessible.

    2. Can you update the article text to make it easier for screen reader users to navigate?

    - There weren’t any real headings, and the comment toggle wasn’t focusable, so I couldn’t use it with the keyboard. I fixed this by turning the font tags into proper headings and paragraphs, which gave the page a clear outline for screen readers.

    3. The navigation menu part of the site (wrapped in <div class="nav"></div>) could be made more accessible by putting it in a proper HTML semantic element. Which one should it be updated to? Make the update.

    - I made the navigation bar use a <nav> element instead of a <div>, which is more semantic and works better with assistive tech.

## The Images
    1. The images are currently inaccessible to screen reader users. Can you fix this?

    - Originally the images didn’t have any alt text, so screen reader users wouldn’t know what they were showing. I added descriptive alt text so they now convey the meaning of the images.

## The Audio Player
    1. The <audio> player isn't accessible to hearing impaired (deaf) people — can you add some kind of accessible alternative for these users?

    - I added transcript below for the audio.

    2. The <audio> player isn't accessible to those using older browsers that don't support HTML audio. How can you allow them to still access the audio?

    - I made the MP3 file to be downloadable for older browsers.

## The Forms
    1. The <input> element in the search form at the top could do with a label, but we don't want to add a visible text label that would potentially spoil the design and isn't really needed by sighted users. How can you add a label that is only accessible to screen readers?

    - I fixed it by adding a label that's only available to screen readers, so sighted users don't see extra text but screen readers announce it correctly.

    2. The two <input> elements in the comment form have visible text labels, but they are not unambiguously associated with their labels — how do you achieve this? Note that you'll need to update some of the CSS rule as well.

    - In the comment form, the two inputs (“Name” and “Comment”) had visible labels but they weren’t properly linked. I fixed that by associating each label with its input using the for and id attributes.

## The Show/Hide Comment Control
    1. The show/hide comment control button is not currently keyboard-accessible. Can you make it keyboard-accessible, both in terms of focusing it using the tab key and activating it using the return key?

    - The comment toggle was just a <div>, so it couldn't be focused or activated with the keyboard. I turned it into a <button> so now it can be reached with Tab and activated with Enter/Space. I also added aria-expanded and aria-controls so screen readers know what it's doing.

## The Table
    1. The data table is not currently very accessible — it is hard for screen reader users to associate data rows and columns together, and the table also has no kind of summary to make it clear what it shows. Can you add some features to your HTML to fix this problem?

    - The data table wasn't accessible because it used <td> instead of <th> in the header row, and it didn't have any summary. I fixed this by changing the header cells to <th> with scope="col", and I added a <caption> that explains the table shows a comparison of wild and urban bears. Now, screen readers can associate the dara with the correct headers.

## Other Considerations?
    1. Can you list two more ideas for improvements that would make the website more accessible?

    - Added a “Skip to main content” link for keyboard users.
    - Made sure focus styles are always visible when tabbing around.