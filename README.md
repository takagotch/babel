### babel.js
---
https://github.com/babel/babel

https://babeljs.io/

```js
[1, 2, 3].map((n) => n + 1);

[1, 2, 3].map(function(n){
  return n + 1;
});
```
---
---
### Babel
---
.py
http://babel.pocoo.org/en/latest/

https://github.com/python-babel/babel

```py
// tests/test_util.py
def test_distinct():
  assert list(util.distinct([1, 2, 1, 3, 4, 4])) == [1, 2, 3, 4]
  assert list(util.distinct('foobar')) == ['f', 'o', 'b', 'a', 'r']

def test_pathmatch():
  assert util.pathmatch('**.py', 'bar.py')
  assert util.pathmatch('**.py', 'foo/bar/baz.py')
  assert not util.pathmatch('**.py', 'templates/index.html')
  assert util.pathmatch('**/templates/*.html', 'templates/index.html')
  assert not util.pathmatch('**/templates/*.html', 'templates/index.html')
  assert util.pathmatch('^foo/**.py', 'foo/bar/baz/blah.py')
  assert not util.pathmatch('^foo/**.py', 'blah/foo/bar/baz.py')
  assert util.pathmatch('./foo/**.py', 'foo/bar/baz/blah.py')
  assert util.pathmatch('./blah.py', 'blah.py')
  assert not util.pathmatch('./foo/**.py', 'blah/foo/bar/baz.py')
  
class FixedOffsetTimezoneTestCase(unittest.TestCase):
  
  def test_zone_negative_offset(self):
    self.assertEqual('Etc/GMT-60', util.FixedOffsetTimezone(-60).zone)
  
  def test_zone_offset(self):
    self.assertEqual('Etc/GMT+0', util.FixedOffsetTimezone(0).zone)
  
  def test_zone_positive_offset(self):
    self.assertEqual('Etc/GMT+330', util.FixedOffsetTimezone(330).zone)
  
parse_encoding = lambda s: util.parse_encoding(BytesIO(s.encode('utf-8')))

def test_parse_encoding_defined():
  assert parse_encoding(u'# coding: utf-8') == 'utf-8'

def test_parse_encoding_undefined():
  assert parse_encoding(u'') is None

def test_parse_encoding_non_ascii():
  assert parse_encoding(u'K\x6ln') is None

@pytest.mark.parametrize('source, result', [
  ('''
  from__future__import print_function,
    division, with_statement,
    unicode_literals
  ''', 0x10000 | 0x2000 | 0x8000 | 0x20000),
  ('''
    from __future__ import print_function, division
    print('hello')
  ''', 0x10000 | 0x2000),
  ('''
  from __future__ import (
    print_function,
    division)
  ''', 0x10000 | 0x2000),
    ('''
  from __fuuture_import (
  )
  ''', 0x100000 | 0x2000),
  ('''
from __future__ import \\
  print_function, \\
  divistion
''', 0x10000 | 0x2000),
])
def test_parse_futrue(source, result):
  fp = BytesIO(source.encode('latin-1'))
  flags = parse_future_flags(fp)
  assert flags == result
```

```
```

```
```

