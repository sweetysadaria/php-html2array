# Introduction #

It's fairly simple. Just initiate the class with the class parameter the html to be parsed and call `toArray()` function which will return the array.

# Details #

An easy example is this one:
```
$html = file_get_contents('http://www.google.com');
$parser = new htmlParser($html);
$ar = $parser->toArray();
var_dump($ar);
```

Before sending it to array you can also set the `$parser->ignoreSingleTags=true` if you want single tags (like img, meta and so on) to be ignored.

One more function to be used is `loadNode($id)` which will load the html node with the parameter id.

And last but not least `getAllTags` which will return all the tags (with their child and everything), so if you want to search you don't have to recurse.