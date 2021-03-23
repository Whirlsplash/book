# Development

## Prerequisites
- [Rust](https://www.rust-lang.org/)
- [Worlds](http://archive.worlds.com/download.html)
- sqlx-cli

## Installing sqlx-cli
Once Rust is installed, run `cargo install sqlx-cli`.

## Setting up database
1. Navigate to the cloned instance of Whirl.
2. Create database file; `sqlx database create`.
3. Migrate database; `sqlx migrate run`.
