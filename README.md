# Left Hand Typing Corrector

A small browser-based typing tool for people who type with their left hand only.

The app lets you type using the left side of the keyboard, then guesses the words you meant by mapping left-hand keys to their mirrored right-hand equivalents.

For example:

```text
jr;;p yp rje wpw;f
```

Can be corrected to:

```text
hello to the world
```

## How it works

The app uses a mirror map between left-hand keys and likely right-hand keys:

```text
q -> p    a -> ;    z -> /
w -> o    s -> l    x -> .
e -> i    d -> k    c -> ,
r -> u    f -> j    v -> m
t -> y    g -> h    b -> n
```

When you type a word, the app generates possible alternatives based on those mappings, then scores them against a small built-in word list and any custom words you have added.

## Getting started

Open `index.html` in your browser. That's it — no build step, no backend, no dependencies.

## Custom words

You can add your own words or short phrases (names, technical terms, anything you use often). They are saved in your browser via `localStorage` and never leave your machine.

## Limitations

This is an early proof of concept.

* The dictionary is small.
* It does not use a real language model.
* Corrections are based on word matching, not sentence context.
* Designed around a standard QWERTY layout.
* It may guess incorrectly when multiple words share the same left-hand pattern.

## License

MIT — see [LICENSE](LICENSE).
