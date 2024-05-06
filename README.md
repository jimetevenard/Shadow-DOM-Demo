# Shadow DOM vs Autofill demo

Web-component libraries like [Material-Web](https://material-web.dev) wrap their input into [shadow DOM instances](https://developer.mozilla.org/en-US/docs/Web/API/Web_components/Using_shadow_DOM)

This allows high-level encapsulation of styles and JS behavior, but could break some credential autofill services.

See
- <https://developer.mozilla.org/en-US/docs/Web/API/Web_components>
- <https://material-web.dev/about/intro/#what-are-web-components>

.

## Simple demo

This small demo reproduces this behavior.

It has two classical username/password inputs.  
It is detected as a login form by most autofiller.

.

If the checkbox is checked, they are wrapped into Shadow DOM instances : their detection could then fail with some autofill services.
