# checkout
CradleCMS (eCommerce) checkout helper web component

Updates the cart whenever `country`, `shipping` or payment `gateway` has been changed.

## Installation
Put the `acheckout.js` component in your themes `components` folder and include it in your `checkout` template. 

It listens on a `change` events originating from the `country` selector, `shipping` address or payment `gateway` and reloads the checkout template.
You must include the `cart.id` either in a form attribute or as a hidden input value.

### Using form data-cart attribute
```
{% form 'checkout' data-cart:cart.id %}
...
{% endform %}
{% component 'acheckout.js' %}
```

### Using hidden input value
```
{% form 'checkout' %}
<input type="hidden" name="cart" value="{{cart.id}}">
{% endform %}
{% component 'acheckout.js' %}
```

> insert the `{% component 'acheckout.js' %}` line after the `<form>` tag.

