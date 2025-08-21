---
layout: post
title: About
permalink: /about/
comments: true
---

## As a conversation Starter

Here are some things that I enjoy.

<comment>
Flags are made using Wikipedia images
</comment>

<style>
    /* Style looks pretty compact, 
       - grid-container and grid-item are referenced the code 
    */
    .grid-container {
        display: grid;
        grid-template-columns: repeat(auto-fill, minmax(150px, 1fr)); /* Dynamic columns */
        gap: 10px;
    }
    .grid-item {
        text-align: center;
    }
    .grid-item img {
        width: 100%;
        height: 100px; /* Fixed height for uniformity */
        object-fit: contain; /* Ensure the image fits within the fixed height */
    }
    .grid-item p {
        margin: 5px 0; /* Add some margin for spacing */
    }

    .image-gallery {
        display: flex;
        flex-wrap: nowrap;
        overflow-x: auto;
        gap: 10px;
        }

    .image-gallery img {
        max-height: 150px;
        object-fit: cover;
        border-radius: 5px;
    }
</style>

<!-- This grid_container class is used by CSS styling and the id is used by JavaScript connection -->
<div class="grid-container" id="grid_container">
    <!-- content will be added here by JavaScript -->
</div>

<script>
    // 1. Make a connection to the HTML container defined in the HTML div
    var container = document.getElementById("grid_container"); // This container connects to the HTML div

    // 2. Define a JavaScript object for our http source and our data rows for the Living in the World grid
    var http_source = "https://upload.wikimedia.org/wikipedia/commons/";
    var living_in_the_world = [
        {"flag": "b/b9/Marvel_Logo.svg", "greeting": "Media", "description": "Marvel - 6 years"},
        {"flag": "f/fc/Valorant_logo_-_pink_color_version.svg", "greeting": "Game", "description": "Valorant - 1 year"},
        {"flag": "f/f2/Roblox_%282025%29_%28App_Icon%29.svg", "greeting": "Game", "description": "Roblox - 7 years"},
        {"flag": "e/ec/Steinway_%26_Sons_upright_piano%2C_model_K-52_%28mahogany_finish%29%2C_manufactured_at_Steinway%27s_factory_in_New_York_City.jpg", "greeting": "Hobby", "description": "Piano - 8 years"},
    ];

    // 3a. Consider how to update style count for size of container
    // The grid-template-columns has been defined as dynamic with auto-fill and minmax

    // 3b. Build grid items inside of our container for each row of data
    for (const location of living_in_the_world) {
        // Create a "div" with "class grid-item" for each row
        var gridItem = document.createElement("div");
        gridItem.className = "grid-item";  // This class name connects the gridItem to the CSS style elements
        // Add "img" HTML tag for the flag
        var img = document.createElement("img");
        img.src = http_source + location.flag; // concatenate the source and flag
        img.alt = location.flag + " Flag"; // add alt text for accessibility

        // Add "p" HTML tag for the description
        var description = document.createElement("p");
        description.textContent = location.description; // extract the description

        // Add "p" HTML tag for the greeting
        var greeting = document.createElement("p");
        greeting.textContent = location.greeting;  // extract the greeting

        // Append img and p HTML tags to the grid item DIV
        gridItem.appendChild(img);
        gridItem.appendChild(description);
        gridItem.appendChild(greeting);

        // Append the grid item DIV to the container DIV
        container.appendChild(gridItem);
    }
</script>

### Fun Facts About Me

-  I enjoy watching Anime
-  I've got into hobbies such as rubix cubes and magic(thought I'm not very good)
-  I enjoy talking to my friends via call or in person
-  I enjoy playing a variety of different game genres
-  I find interest in romance or fantasy novels/books
-  My favorite drink is milk 
-  I love all types of cuisines
-  Some of my favorite food is sushi and ramen

### Culture, Family, and Fun

Most of my world revolves around my family and friends

- My nationality is American, my Ethinicity is Indian, and my name is Irish.
- I love my parents and have a good relationship with them. I also have a brother who is two years older than I am. My brother and I share similar hobbies, and I also enjoy interests that my parents introduced me to, which we love bonding over together.
- The gallery has pics of me, my family and my friends

<comment>
Gallery of Pics, scroll to the right for more ...
</comment>
<div class="image-gallery">
  <img src="{{site.baseurl}}/images/about/family1.jpg" alt="Image 1">
  <img src="{{site.baseurl}}/images/about/family2.jpg" alt="Image 2">
  <img src="{{site.baseurl}}/images/about/family3.jpg" alt="Image 3">
  <img src="{{site.baseurl}}/images/about/family4.jpg" alt="Image 4">
  <img src="{{site.baseurl}}/images/about/family5.jpg" alt="Image 5">
  <img src="{{site.baseurl}}/images/about/family6.jpg" alt="Image 6">
  <img src="{{site.baseurl}}/images/about/family7.jpg" alt="Image 7">
  <img src="{{site.baseurl}}/images/about/family8.jpg" alt="Image 8">
</div>
