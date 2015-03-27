The PHP class takes a string containing HMTL code and parses it to an array as good as possible (it tries to do its best even if the code is malformed).
The class works inverse than others. It parses from the simplest HTML tags to the complex ones.
It works fairly fast. It has the option to ignore single tags (such as meta tags, img tags and so on).

An easy example is this one:
```
$html = file_get_contents('http://www.google.com');
$parser = new htmlParser($html);
$ar = $parser->toArray();
var_dump($ar);
```