# imageSearch
const accessKey = "RZEIOVfPhS7vMLkFdd2TSKGFBS4o9_FmcV1Nje3FSjw";: This is an access key that is used to authenticate with the Unsplash API. It's required to access the image data.

const form = document.querySelector("form");: This line selects an HTML form element on the web page. This form will be used to input the search query.

const searchInput = document.getElementById("search-input");: This line selects an HTML input element with the id "search-input". This input field is where the user enters their search query.

const searchResults = document.querySelector(".search-results");: This line selects an HTML element with the class "search-results". This element will be used to display the search results (images).

const showMoreButton = document.getElementById("show-more-button");: This line selects an HTML button element with the id "show-more-button". This button will allow users to load more search results.

let inputData = "";: This variable will be used to store the user's search query.

let page = 1;: This variable keeps track of the current page of search results. It starts at page 1.

async function searchImages() { ... }: This is a JavaScript function called searchImages. It performs the main functionality of searching for images and displaying them.

Inside the searchImages function:

It first stores the user's input (search query) in the inputData variable.
Then, it constructs a URL to request image data from the Unsplash API using the search query and the access key.
It makes an asynchronous HTTP request (using await fetch(...)) to the Unsplash API to get image data based on the search query.
It processes the response data, creating HTML elements for each image result and appending them to the searchResults element.
It increments the page variable to load more results as the user clicks the "Show More" button.
If it's not the first page of results, it displays the "Show More" button.
form.addEventListener("submit", (event) => { ... });: This code adds an event listener to the form. When the user submits the form (by pressing Enter or clicking a submit button), it prevents the default form submission (which would cause the page to reload) and calls the searchImages function to start the search from the first page.

showMoreButton.addEventListener("click", () => { ... });: This code adds an event listener to the "Show More" button. When the user clicks the button, it calls the searchImages function to load more search results.
