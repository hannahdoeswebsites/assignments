# Create Your Own Etsy Search Page

## Description
This exercise utilizes Handlebars templates to re-create the Etsy search results page.


## Objectives

### Learning Objectives

After completing this assignment, you should…

- Understand JavaScript templating
- Demonstrate strong ability to navigate through a large block of JSON data

### Performance Objectives

After completing this assignment, you be able to effectively use

* Handlebars.js
* JSON data


## Details

### Deliverables

* A repo containing at least:
  * `main.js`
  * `index.html`

### Requirements

## Normal Mode

Re-Create An Etsy Page - https://www.etsy.com/search?q=whiskey

> Specifically you need to focus on the sidebar and the main content of items. 

1. Utilize the data for whatever search term you use - [DATA
   HERE](https://api.etsy.com/v2/listings/active.js?api_key=cdwxq4soa7q4zuavbtynj8wx&keywords=whiskey&includes=Images,Shop&sort_on=score)
2. Use Bourbon / Neat to help you out (optional, but suggested)
3. You are free to change the search term to whatever you'd like.
4. We haven't covered how to fetch data using JavaScript, so just copy the function done during the Marvel demo.
5. Everything should be styled as closely as possible, including the Header/Footer
6. You should implement hover events and link the items to their proper Etsy product pages
7. Unless you do the bonus question #2, you can just put random links in your sidebar.
8. Also, no need to make any of the form elements work.

## Hard Mode

Everything above plus:

1. Create your own API token by signing up as an [Etsy developer](https://www.etsy.com/developers/)
2. Pull the categories from the data to create the sidebar, with links that filter the listings.
3. Implement the sorting dropdown.

## Additional Resources

- [Handlebars.js documentation](http://handlebarsjs.com/)

- [Etsy API Documentation](https://www.etsy.com/developers/documentation/reference/listing)
- [Etsy Payload
  Example](https://api.etsy.com/v2/listings/active.js?api_key=cdwxq4soa7q4zuavbtynj8wx&keywords=tacos&includes=Images,Shop&sort_on=score)
- [Etsy Page Example](https://www.etsy.com/search?q=tacos)

### Installing Handlebars
1. In your project directory: `bower install --save handlebars`
2. Link to the handlebars library: `<script
   src="bower_components/handlebars/handlebars.js"></script>`

### Fetching data from Etsy
You will need to use the following function to fetch data from Etsy's API. You
call the function with the API URL as well as a callback function that will
receive the response.

```js
function fetchJSONP(url, callback) {
    var callbackName = 'jsonp_callback_' + Math.round(100000 * Math.random());
    var script = document.createElement('script');

    window[callbackName] = function(data) {
        delete window[callbackName];
        document.body.removeChild(script);
        callback(data);
    };

    script.src = url + (url.indexOf('?') >= 0 ? '&' : '?') + 'callback=' + callbackName;
    document.body.appendChild(script);
}
```

Then you can call the function like this, where you would replace `logResults`
with the name of the function you want to be called with the results.

```js
var url = "https://api.etsy.com/v2/listings/active.js?api_key=cdwxq4soa7q4zuavbtynj8wx&keywords=tacos&includes=Images,Shop";
fetchJSONP(url, logResults);
```
