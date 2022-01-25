# jQuery Warn Before Unload

Prevents a page from unloading directly when something was changed in any input or text area. Asks whether you are sure or not.

## Getting started

Add with yarn or npm:
```
yarn add jquery-warn-before-unload
```

Then include javascript, for example like that (in a rails project):
```
//= require jquery-warn-before-unload/jquery.warnBeforeUnload
```

## Usage

Any input / select field change triggers an alert if you try to leave the page without saving.
We consider that a form submission clears the alert.

Basically you have some code like that in your html:
```
<form>
  <input type="text" name="myfield">
  <input type="submit">
</form>
```
If you change the text input and try to leave the page (by clicking any link or refresh on your browser) you will trigger the warning. If you just submit the form the warning will not be triggered.

## Exceptions

Please note that inputs/selects with any of those classes: `do-not-warn-before-unload`, `filter` will be ignored and will not trigger the alert.
Input type `search` won't trigger the alert either.
Also note that a form with a class `do-not-unlock` will not remove the alert.
