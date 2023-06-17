# URL based Preview Widget

## Summary
In addition to our current product based preview widget, URL based widget adds the ability to enable a playlist in non-product pages. Any page can embed the widget with a fully customizable playlist.

## URL widget

URL based widget is organised per site. Different sites can have different URLs. A URL can be created under site page:

![image](https://github.com/preview-dev/docs/assets/136892816/c7b51d6b-3488-4c9a-88fe-8da87060fe5d)


Then you can create a URL resource as below:

![image](https://github.com/preview-dev/docs/assets/136892816/d2911eb5-3ef3-4254-82f6-16cf7abd41b6)


Once the URL is saved successfully, you should be able to see the URL details page as below:

![image](https://github.com/preview-dev/docs/assets/136892816/04ad80ef-556f-4f9d-b508-04d2aacc6136)


The next step is configure the playlist for it. There are two kinds of URL based playlist:

1. Products Group playlist
2. Customizable dedicated playlist dedicated for the widget

###  Products Group Playlist

For this playlist, the URL should be configured to be associated with multiple products. The playlist of the URL is an aggregation of all products’ linked videos (sampled by top 5 randomly).

You can search the products and link the product to the URL directly in the above page. 

![image](https://github.com/preview-dev/docs/assets/136892816/8ced3948-0d0d-4a07-bef4-237ceed3ceb7)

Alternatively, you can go to product details page:

![image](https://github.com/preview-dev/docs/assets/136892816/bdd06897-277a-40b0-8e53-af52465647cf)

Then choose the target URL you would like to link:

![image](https://github.com/preview-dev/docs/assets/136892816/844ff4ac-d8bb-4ada-b780-19919dda59f1)


### Dedicated Playlist

URL based playlist can be fully customised. It could be done via a concept called Virtual Product. You can create a Virtual Product and draft a playlist for it. Then link the virtual product solely to the target URL.

![image](https://github.com/preview-dev/docs/assets/136892816/624306b9-6b74-47e0-9b64-ee1d3dd72214)

![image](https://github.com/preview-dev/docs/assets/136892816/4f886ed4-353a-4a23-bffd-e29fc6155663)

## Website Configuration

Choose a page and/or location for the playlist
Similar to the product specific playlist, a script as below should be placed in the target location

```html
<div class="previewUrl" />
```

Then add widget via the below code piece:
```html
(function (w,d,s,o,f,js,fjs) {
		w[o] = w[o] || function () { (w[o].q = w[o].q || []).push(arguments) };
        js = d.createElement(s), fjs = d.querySelector('.'+o);
        js.id = o; js.src = f; js.async = 1; fjs.parentNode.insertBefore(js, fjs);
    }(window, document, 'script', 'previewUrl', 'https://widget.preview.io/preview.js'));

previewUrl('url', {mode: "section"});
```

