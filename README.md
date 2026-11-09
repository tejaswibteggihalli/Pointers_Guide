# C Pointers Field Guide

An interactive, single-page guide to C pointers. Step through memory one line at a time, play with pointer arithmetic, and drill 70 edge-case questions on the things that actually bite: dangling pointers, off-by-one errors, `const` placement, `realloc` surprises, undefined behavior and more.

No build step, no dependencies, no install. Open the HTML file in a browser.

## Who it's for

- Beginners meeting `*` and `&` for the first time
- Students who "get" pointers until arrays, `const` and `**` show up
- Anyone preparing for a systems or C interview
- Experienced programmers who want a quick refresher on the sharp edges

You do not need any background beyond basic C syntax (variables, functions, arrays).

## What's inside

| Section | What it does |
| --- | --- |
| **Step through memory** | Five scenes (pointer basics, pointer to pointer, arrays and `p + 2`, swap with pointers, heap with `malloc`/`free`/dangling). Press Next step and watch variables, addresses and arrows update as each line runs. |
| **Arithmetic lab** | Pick `char`, `short`, `int` or `double`, slide the offset, and see exactly which bytes `*(p + i)` would touch, including one past the end and before the start. |
| **Memory maps** | Side-by-side layout of a typical 64-bit Linux process (stack, heap, `.bss`, `.data`, `.rodata`, `.text`) and a minimal 16-bit teaching machine. |
| **Edge-case drill** | 70 questions in 7 topics: Basics, Declarations & const, Arrays & pointer arithmetic, Strings, Stack/heap & lifetime, Pointers & functions, Structs, Undefined behavior, Debugging & tools. Reveal answers, mark "Got it" or "Review later", filter by topic, search. Progress is saved in your browser. |
| **Cheat sheet** | Symptom, cause and fix table, ten rules for safe pointer code, and an operator precedence quick reference. |

## Using it

1. Download `C Pointers Field Guide.html`.
2. Open it in any modern browser.

Works on desktop and mobile, in light and dark mode. Web fonts load from Google Fonts when online and fall back to system fonts offline.

Your drill progress is stored in `localStorage`, so it stays on the device and browser you used. "Clear marks" resets it.

## Optional extra: the "Hack" panels

Some panels (the small assembly box under each memory scene, and the "Hack to C" comparison table) map C pointers onto a minimal 16-bit computer. They are there for readers who have built or studied such a machine, for example through the nand2tetris course. If you haven't, ignore them; every explanation, example and question in the guide stands on its own in plain C terms.

## Assumptions

Examples assume a 64-bit little-endian system and C11 or later. Behavior marked undefined is undefined by the C standard regardless of platform. When trying the examples yourself, compile with:

```sh
gcc -std=c17 -g -O0 -Wall -Wextra -Wpedantic -fsanitize=address,undefined main.c -o main
```

## Credits

This project was made entirely with [Claude](https://claude.ai), Anthropic's AI assistant: the content, the interactive visualizers, the design and the code.

## License

Add the license of your choice here.
