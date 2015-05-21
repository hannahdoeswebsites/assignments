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
   HERE](https://api.etsy.com/v2/listings/active?api_key=cdwxq4soa7q4zuavbtynj8wx&keywords=whiskey&includes=Images,Shop&sort_on=score)
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

- [Etsy API Documentation](https://www.etsy.com/developers/documentation/reference/listing)
- [Etsy Payload
  Example](https://api.etsy.com/v2/listings/active?api_key=cdwxq4soa7q4zuavbtynj8wx&keywords=tacos&includes=Images,Shop&sort_on=score)
- [Etsy Page Example](https://www.etsy.com/search?q=tacos)
