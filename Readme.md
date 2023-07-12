# Autocomplete Keyhead Search Engine using Alpine JS

This is a simple search engine that uses Alpine JS to provide a dropdown of search results as the user types in their query. It fetches data from Reddit's search API and displays the results in a dropdown list. The user can navigate through the list using the arrow keys and select a result by pressing enter.

### Getting Started

To use this search engine, you need to include the following dependencies in your HTML file:

- Alpine JS
- jQuery
- Popper.js
- Bootstrap CSS and JS

You can include these dependencies using their respective CDN links like in the example code above.

### Usage

To use this search engine, you need to create an HTML input field and add the `x-data` attribute to it with the value of `dropdownSearch()`. This will initialize the Alpine JS component and bind it to the input field.

```html
<input type="text" class="mt-5 rounded-md border focus:border-indigo-300 w-full px-4 py-2"
    placeholder="Search" x-model="query" x-on:click.outside="reset()" x-on:keyup.escape="reset()"
    x-on:keyup.down="selectNext" x-on:keyup.up="selectPrevious" x-on:keyup.enter="goUrl()" autofocus
    x-data="dropdownSearch()">
```

### Customization

You can customize the search engine by modifying the CSS classes used in the HTML code. For example, you can change the color of the search bar by modifying the `text-primary` class.

You can also modify the search API used by changing the URL in the `data_search` function. Currently, it uses Reddit's search API, but you can replace it with any other search API that returns results in JSON format.

### Conclusion

That's it! You now have a simple autocomplete keyhead search engine that you can use on your website. Feel free to customize it further to suit your needs.
