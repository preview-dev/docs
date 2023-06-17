## Install Preview Widget 

To get Preview Widget installed in your website, you need to inject some HTML and Javascript snippets in your website. 

Firstly, place the below HTML code in a location where you'd like the Preview Widget to be displayed.

```html
<div class="preview"></div>
```

Then place the below code anywhere in the HTML page. It is suggested to place in the ending of html body.

```html
</script><script type="text/javascript">
(function (w,d,s,o,f,js,fjs) {
w[o] = w[o] || function () { (w[o].q = w[o].q || []).push(arguments) };
    js = d.createElement(s), fjs = d.querySelector('.'+o);
    js.id = o; js.src = f; js.async = 1; fjs.parentNode.insertBefore(js, fjs);
 	}(window, document, 'script', 'preview', 'https://widget.preview.io/preview.js'));

preview("searchv2", {
  element: '{PRODUCT-TITLE-SELECTOR}',
  skuSelector: '{PRODUCT-SKU-SELECTOR}'
});

preview('loadv2', {
    element: '{PRODUCT-TITLE-SELECTOR}',
    form: '{PRODUCT-FORM-SELECTOR}',
    priceSelector: '{PRODUCT-PRICE-SELECTOR}',
    mode: '{MODE}',
    carouselSelector: "{PRODUCT-IMAGE-SELECTOR}"
  });
</script>
```

| Variable Name | Description |
| ----------------------  | --- |
| PRODUCT-TITLE-SELECTOR  | css selector for the product's title    |
| PRODUCT-SKU-SELECTOR    | css selector for the product's sku, sku is used to uniquely identify a product regardless of the possible name changes    |
| PRODUCT-FORM-SELECTOR   | css selector for the product's purchase form, optinoal    |
| PRODUCT-PRICE-SELECTOR  | css selector for the product's price, optional    |
| PRODUCT-IMAGE-SELECTOR  | css selector for the product's image, optional    |
| MODE                    | The mode of the widget, it is suggested to use either `section` or `section-tabs`, for more details, see the below section.    |  

## Configure the widget

### Mode

#### section
The most popular mode which would displays the Youtube player directly embedded in your product page.

![image](https://github.com/preview-dev/docs/assets/136892816/c1a4974c-9736-494f-bc00-420ee7535e7b)


#### section-tabs
This mode can support mutilple styles of videos, like Youtube, Youtute Shorts. Tiktok could be added in the future as well.

#### widget
A preview widget is displayed instead of the section mode. Once the widget is clicked, a modal would be showed up to display the Youtube player and playlist.

#### widget-fullscreen
Unlike the widget mode, this mode would open the player in a fullscreen mode in your product page.

#### section-fullscreen
Unlike the section mode, this mode would open the player in a fullscreen mode in your product page.
