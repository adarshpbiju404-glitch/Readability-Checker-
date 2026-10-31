# Readability and Keyword Density Checker

Paste any article, blog post or landing page copy and see how readable it is, how long it takes to read, and which words and phrases it leans on most. Runs entirely in the browser, so nothing you paste is uploaded.

**Live demo:** `https:///adarshpbiju404-glitch.github.io/readability-keyword-checker/`


## Why I built this

Good SEO writing has to work for two audiences: readers who skim and search engines that look for the right topics. Most free checkers either bury you in jargon or push a signup. I wanted something quick that shows what matters while you write: reading level, sentence length and keyword use.

## Features

- Write and Edit modes. In Edit mode the text is highlighted line by line: red for very hard sentences, yellow for hard ones, blue for adverbs, green for passive voice, and purple for phrases that have simpler alternatives (hover for the suggestion)
- Sidebar with a grade level, counts for each highlight type, and totals for words, characters, paragraphs, sentences, reading time and Flesch reading ease
- Most used single words, two-word and three-word phrases, with counts and density
- Target keyword tracker: uses, density, and whether it appears in the first 100 words
- Dark theme for low-light work
- Single HTML file, no build step, no dependencies, no tracking

## How the numbers work

- **Grade level** uses the Automated Readability Index: 4.71 x (characters per word) + 0.5 x (words per sentence) - 21.43
- **Hard and very hard sentences** are sentences of 14 words or more whose own grade is 10 to 13 (hard) or 14 and above (very hard)
- **Adverbs** are words ending in "ly", with a list of common exceptions such as "family" and "early"
- **Passive voice** is a form of "to be" followed by a past participle, so a few false positives are possible
- **Simpler alternatives** come from a built-in list of about 40 wordy phrases, which you can extend in the `SIMPLE` object in `index.html`
- **Flesch reading ease** = 206.835 - 1.015 x (words per sentence) - 84.6 x (syllables per word). Syllables are counted with a simple vowel-group rule, so results are close but not exact
- **Reading time** assumes 230 words per minute
- **Keyword density** = number of uses divided by total words. The 0.5% to 2.5% range is a common rule of thumb, not a search engine rule
- Common filler words (the, and, of and similar) are ignored in the word lists

Inspired by the Hemingway Editor. This is an independent project and does not use its code.


## Run it locally

Open `Readability.html` in any browser.

## Roadmap

- Highlight target keywords inside the text
- Edit the text directly in the highlighted view
- Compare two drafts side by side
- Companion tool: 30-day content calendar generator


