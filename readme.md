# Multi OS development setup guide

Little bit of personal documentation built with `mdbook`.

## Setup of an `mdbook`

First get Rust set up with cargo, and then run:

```bash
cargo install mdbook
```

and initialise a new directory for your book:

```bash
mdbook init direcctory-name
```

This will ask you if you want a `.gitignore` and what title to give the main page of your book/doc (you can change that later of course in the `book.toml`).

navigate into that folder and you can do:

```bash
mdbook serve
```

to host it live.

## Usage

Place your `.md` files in the src folder and link them up to the `SUMMARY.MD` file. The title and author are set in the `book.toml` file.