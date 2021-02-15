# Python 3 String to Emoji Hash

Hash a unicode string to emoji.

[kawa-kokosowa/pymojihash](https://github.com/kawa-kokosowa/pymojihash) fork
based on the npm package [hash-emoji by
earobinson](https://github.com/earobinson/hash-emoji).

You can run tests simply by running `pytest`.

## Examples

`hash_to_emoji()` is the wonderful hashing function.

In this example a string is hashed to a single emoji:

```python
from pymojihash import hash_to_emoji
hash_to_emoji('lol')
'🇫🇲'
```

There is a limited number of emojis outputs (see: `emojis.json` in this
package) so if you increase the `hash_length` the less likely you are to
encounter different values which produce the same output/hash/emoji(s):

```python
hash_to_emoji('lol', 4)
'◼️🍕🍐🇫🇲'
hash_to_emoji('lol', 2)
'🍐🇫🇲'
hash_to_emoji('heck', 2)
'♠️🇨🇦'
```
