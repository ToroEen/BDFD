# Line Splitter
The goal is to split an input into lines witch individually will be run through the parser. 

# Current, not working version
**Input**
```js
var test = "temp"
test.value
test.name
```
**Code**
```php
$var[t;$replaceText[$message;
;@;-1]]

$var[c;1]

$eval[%{DOL}%var[line$var[c]\;$replaceText[$var[t];@;\]%{DOL}%var[c\;%{DOL}%sum[%{DOL}%var[c\]\;1\]\]%{DOL}%var[line%{DOL}%var[c\]\;;-1]\]]

L1: $var[line1]
L2: $var[line2]
L3: $var[line3]
```
**Output**
```js
L1: var test = "temp"
L2: test.value
L3: test.name
```
# Things that need to change
This part:
```php
L1: $var[line1]
L2: $var[line2]
L3: $var[line3]
```
Shouldn't be predefined and instead generated by code depending on the amount of lines existing. Which is the value of `$var[c]`.
Feel free to come up with solutions.

(btw thats not the only issue yet, but its a great start to fix this one first.)
