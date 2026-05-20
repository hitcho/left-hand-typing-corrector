````markdown
# Left Hand Typing Corrector

A small browser-based typing tool for people who type with their left hand only.

The app lets you type using the left side of the keyboard, then guesses the words you meant by mapping left-hand keys to their mirrored right-hand equivalents.

For example:

```text
jr;;p yp rje wpw;f
````

Can be corrected to:

```text
hello to the world
```

## Why this exists

Most typing tools assume the user has access to both hands. This project explores a simple idea:

What if someone could type with their left hand only, and the software could infer the intended right-hand letters?

It is not trying to be perfect. It is a lightweight proof of concept that runs entirely in the browser.

## Features

* Single-file HTML app
* No build step
* No backend
* No external dependencies
* Live correction as you type
* Left-hand to right-hand mirror key mapping
* Built-in dictionary
* Phrase correction examples
* Custom word storage using `localStorage`
* Copy corrected text
* Replace typed input with corrected output

## How it works

The app uses a mirror map between left-hand keys and likely right-hand keys.

Example mappings:

```js
q -> p
w -> o
e -> i
r -> u
t -> y

a -> ;
s -> l
d -> k
f -> j
g -> h

z -> /
x -> .
c -> ,
v -> m
b -> n
```

When you type a word, the app generates possible alternatives based on those mappings, then scores them against a small built-in word list and any custom words you have added.

## Getting started

Clone the repo:

```bash
git clone https://github.com/hitcho/left-hand-typing-corrector.git
cd left-hand-typing-corrector
```

Open the file in your browser:

```bash
open index.html
```

Or just double-click `index.html`.

## Publishing with GitHub Pages

1. Create a new GitHub repository.
2. Add the HTML file as `index.html`.
3. Push it to GitHub.
4. Go to your repo settings.
5. Open **Pages**.
6. Under **Build and deployment**, choose:

   * Source: `Deploy from a branch`
   * Branch: `main`
   * Folder: `/root`
7. Save.

Your app will be available at:

```text
https://hitcho.github.io/left-hand-typing-corrector/
```

## Suggested repo structure

```text
left-hand-typing-corrector/
├── index.html
├── README.md
└── LICENSE
```

## Custom words

The app lets you add your own words or short phrases, such as names, technical terms, or words you use often.

Custom words are saved in your browser using `localStorage`.

They are not uploaded anywhere.

## Limitations

This is an early proof of concept.

Current limitations:

* The dictionary is small.
* It does not use a real language model.
* Corrections are based on word matching, not deep sentence context.
* Keyboard layout support is currently designed around a standard QWERTY layout.
* It may guess incorrectly when multiple words share the same left-hand pattern.

## Future ideas

Possible improvements:

* Add a larger dictionary
* Support custom keyboard layouts
* Add phrase-level prediction
* Add word frequency scoring
* Add export and import for custom words
* Add accessibility settings
* Add offline PWA support
* Add a training mode that learns from accepted corrections

## Privacy

Everything runs locally in your browser.

No text is sent to a server.

Custom words are saved only in the browser where you added them.

## License

MIT License.
