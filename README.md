# code-snippets

Just code. Currently, only [Sass](http://sass-lang.com) code, like mixins and placeholders.

## meet `equal-height()`
This is a simple Sass mixin I created it a long time ago for achieving equal height columns without flexbox.
> [Live example](http://codepen.io/diessica/full/ZGNXXd).

### usage

HTML structure, where `nav` and `section`s are **siblings** (share the same parent element).

```html
<nav>Sidebar navigation</nav>
<section>A random section of content</section>
<section>Another section of content</section>
```

Sass
```sass
section, nav
  +equal-height
```

Done! `nav`, and both `section`s got the same height.

It doesn't matter the content, how many columns you have, neither the `nav` nor `section`'s `height`, nor if you don't have a container wrapping the siblings. **It just works**, and without neither `position: absolute` nor `background-image`.

If displaying the parent  as `table`s and the children as `table-cell`s isn't a problem for your code at all, just use it. Since you are not using actual tables, there's no reason to feel bad here.

> **Note:** `display: table` always will inherit to the parent element `body` unless you set `$wrapper` (see below).

### options
##### $wrapper
It sets a wrapper for the columns.

Type: `string` <br>
Default: `body`


# to-do
- [ ] Documentation for Sass snippets.

---

###### LICENSE

[![CC0](http://mirrors.creativecommons.org/presskit/buttons/88x31/svg/cc-zero.svg)](http://creativecommons.org/publicdomain/zero/1.0/)

To the extent possible under law, [Diéssica Gurskas](http://diessi.ca) has waived all copyright and related or neighboring rights to this work.
