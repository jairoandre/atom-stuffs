# Operator Mono Alternative

Download and install both FiraCode and FlottFlott (or another cursive alternative if you want)

Fira Code is an extension of the Fira Mono font containing a set of ligatures for common programming multi-character combinations. This is just a font rendering feature: underlying code remains ASCII-compatible. This helps to read and understand code faster. You an download Fira Code on Github https://github.com/tonsky/FiraCode

FlottFlott is a free font I found on dafont.com that I think works well with code. To find a cursive font that works well with code can be a bit daunting, I know because I downloaded at least a couple dozen before deciding that FlottFlott was right for me. Can you find a better one? If so let me know I’d love to make this even better if I can. You can download FlottFlott on Dafont at http://www.dafont.com/flottflott.font

After installing the two fonts, paste this code into your styles.less file in Atom

```css
atom-text-editor {
  font-family: 'Fira Code';
  font-style: normal;  
  text-rendering: optimizeLegibility;
}
atom-text-editor::shadow {
  .string.quoted,
  .string.regexp {
    -webkit-font-feature-settings: "liga" off, "calt" off;
  }
  .source.js.jsx > .keyword.control.flow.js,
  .storage, .type .function {
    vertical-align: baseline;
    font-family: 'flottflott';
    height: inherit;
    font-size: 1.5em;
    line-height: 1rem;
  }
  .source.js.jsx,
  .storage.type.function.arrow.js,
  .variable {
    font-family: 'Fira Code';
    font-style: normal;
  }
  .string.unquoted.js {
    color: #CDD3DE;
  }
  .entity.name {
    font-weight: bold;
  }
}
```
You should now have some cool looking code with ligatures. If you don’t, please leave a comment so I can revise this. Also, sorry this is only explained for atom right now, I do plan on sharing how this can be done with VS code as well.
If you want the same coloring, you can use Oceanic Next as the syntax theme.
Let me know if you found this guide useful or if it was missing something critical.

https://medium.com/@docodemore/an-alternative-to-operator-mono-font-6e5d040e1c7e#.3q9ywwphp
