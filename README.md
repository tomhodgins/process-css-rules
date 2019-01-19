# process-css-rules

Process every rule in a CSS stylesheet object with a JavaScript callback function

## about

Useful when you need to operate on individual style rules and provides an easy way to read information out of, or dynamically update selectors, properties and values found in CSSOM.

This can be used for CSS preprocessing, one-time processing in the browser or to provide a way to transform CSS for dynamically generated styles (useful for things like style scoping, element/container queries, and modularizing styles to make things self-contained).

## usage

This software is distributed as an ES module and should work in all modern browsers (including Chrome/Safari/Edge/Firefox).

```js
import processRules from 'https://unpkg.com/process-css-rules/index.js'

// Log text of all rules found in CSSOM to the console
Array.from(document.styleSheets).forEach(stylesheet =>
  processRules(stylesheet, rule => console.log(rule.cssText))
)
```