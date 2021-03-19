# Workflow

## Prerequisites
- A Java decompiler. I think [Java Decompiler](https://java-decompiler.github.io/) is a neat one.
- Setting the `netdebug` flag within your `worlds.ini` file to `255`.

## Process
1. Run Worlds, login, walk around, just gather some sample data.
2. Open your `Gamma.log` file within a text editor.
3. Open Java Decompiler and drag your `worlds.jar` onto it; opening it.
4. Within your `Gamma.log`, find a network request, e.g
`[18803] test.3dcd.com:6650: send(BUDDYLISTUPDATE  fuwn 1)`.
5. Note the command used, e.g. `BUDDYLUSTUPDATE`.
6. Within Java Decompiler, bring up the Search feature using `Ctrl+Shift+S` and tick all the search options.
7. Profit.

### Extended
For `BUDDYLISTUPDATE`, I ended up in the `NET.worlds.network.BuddyListUpdateCmd` class.

Here, I can review the methods which this class contains, and I notice that one happens to have 
the name `send`. 

I can now reference the raw packet data from a network proxy like Wireshark with this 
method and connect the dots.
