# Okizeme Browser Shortcut

This is a browser shortcut helper for the [Okizeme Tekken 8 database](https://okizeme.gg/database).

It lets you jump to character pages, search moves, or open exact move pages directly from your browser address bar.

Instead of opening Okizeme, selecting a character, and typing a move into the search box, you can type something like:

```text
@okizeme kuni d1+2
```

and go straight to Kunimitsu's Okizeme page with `d1+2` searched.

## What It Does

The shortcut understands Tekken 8 character names and common aliases.

For example:

```text
@okizeme jack d1+2
```

opens the Okizeme page for Jack-8 and searches for `d1+2`.

It also supports short names:

```text
@okizeme kuni SET1+2
@okizeme dj u4
@okizeme ak df1
```

These resolve to:

```text
kuni  -> kunimitsu
dj    -> devil-jin
ak    -> armor-king
yoshi -> yoshimitsu
jack  -> jack-8
```

## Adding It To Your Browser

The shortcut works by adding a custom search engine / site search entry in your browser.

Use this URL:

```text
https://uberspy.github.io/okizeme-shortcut/?q=%s
```

That URL expects the redirect file to be published as `index.html` in the GitHub Pages site. The `README.md` is only the project documentation shown on GitHub.

Use whatever keyword you prefer. The examples below use:

```text
@okizeme
```

### Chrome / Edge

1. Open browser settings.
2. Go to `Search engine`.
3. Open `Manage search engines and site search`.
4. Add a new site search.
5. Set the shortcut keyword to `@okizeme`.
6. Set the URL to:

```text
https://uberspy.github.io/okizeme-shortcut/?q=%s
```

After that, type `@okizeme`, press space or tab, then type your search.

### Firefox

Firefox custom search setup depends on your version and settings.

The usual approach is:

1. Bookmark the shortcut page.
2. Edit the bookmark.
3. Add a keyword such as `@okizeme`.
4. Use this as the bookmark URL:

```text
https://uberspy.github.io/okizeme-shortcut/?q=%s
```

Then type the keyword and your query in the address bar.

## How To Use It

### Open The Database

```text
@okizeme
```

Opens:

```text
https://okizeme.gg/database
```

### Open A Character Page

```text
@okizeme jin
```

Opens:

```text
https://okizeme.gg/database/jin
```

### Search For A Move

```text
@okizeme jack d1+2
```

Opens Jack-8's page and searches for `d1+2`.

This is the recommended default mode because it does not require exact Okizeme move-page notation.

More examples:

```text
@okizeme kaz df2
@okizeme reina ff2
@okizeme kuni SET1+2
@okizeme devil jin u4
@okizeme armor king throw
```

## Direct Move Pages

If you add a direct-mode flag to the end, the shortcut tries to open the exact move page instead of using search.

```text
@okizeme kuni d1+2 direct
```

Short flag forms work too:

```text
@okizeme kuni d1+2 d
@okizeme kuni d1+2 -d
@okizeme kuni d1+2 --direct
```

Direct mode is useful when you know the move exists and want the move page immediately.

Okizeme's direct move URLs require stricter notation, so the shortcut fixes common Tekken shorthand automatically.

Examples:

```text
d1+2     -> d+1+2
df1      -> df+1
df 1     -> df+1
d/f1     -> df+1
SET1     -> SET.1
SET1+2   -> SET.1+2
set 1+2  -> SET.1+2
```

So this:

```text
@okizeme kuni SET1+2 direct
```

opens the same direct page as Okizeme's stricter notation:

```text
SET.1+2
```

## Character Aliases

You can use full names, common names, or short aliases.

Examples:

```text
alisa
anna
armor king / ak
asuka
azucena
bryan
claudio
clive
devil jin / dj
dragunov
eddy
fahkumram / fahk
feng
heihachi
hwoarang / hwo
jack / jack-8
jin
jun
kazuya / kaz
king
kuma
kunimitsu / kuni
lars
law
lee
leo
leroy
lidia
lili
miary zo / miary
nina
panda
paul
raven
reina
shaheen
steve
victor
xiaoyu / ling
yoshimitsu / yoshi
zafina
```

Season 3 DLC aliases are included too:

```text
bob
roger jr / roger
yujiro hanma / yujiro
```

## Recommended Use

Use normal search mode most of the time:

```text
@okizeme character move
```

Use direct mode when you want to jump straight to a specific move page:

```text
@okizeme character move direct
@okizeme character move d
```

Search mode is more forgiving. Direct mode is faster when the notation matches an Okizeme move page.
