### Sublime Text 3 snippet for wrapping string into a Translation String 

I often use Translation Strings on multilang websites, and once I get bored of typing blade's template literals, I created this snippet.

You can read more in the Laravel docs about Translation Strings: https://laravel.com/docs/5.5/localization#defining-translation-strings

#### 1. Create a new snippet (Tools / Developer / New snippet on Linux)

```bash
<snippet>
    <content><![CDATA[{{ __('$SELECTION') }}]]></content>    
    <scope>source.php</scope> -->
</snippet>
```
Save as `wrapcustom` or anything you like. We don't need a trigger keyword, so I deleted that part.

#### 2. Create a new keybinding (Preferences / Key Bindings on Linux)

Add this to the `User` config. Check if the key combination isn't used yet. If yes, choose a different one.

```bash
{ "keys": ["ctrl+shift+o"], 
  "command": "insert_snippet", 
  "args": { "name": "Packages/User/wrapcustom.sublime-snippet" } 
},
```
#### 3. Finally, select a string/text and press the snippet activation keys (for me CTRL+SHIFT+O)

From this
```bash
Select this
```
will be
```bash
{{ __('Select this') }}
```