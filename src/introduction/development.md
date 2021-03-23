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

## Overwriting WorldServer address
1. Navigate to your `/etc/hosts` file, on Windows this is usually located at
   `C:\Windows\System32\drivers\etc\hosts`.
2. Add these rules;
	```
	0.0.0.0				www.3dcd.com
	0.0.0.0				test.3dcd.com
	```
