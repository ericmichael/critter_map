# Critter Map

For this assignment, you're going to practice AJAX and page manipulation again, but just to change it up you'll be moving pictures around instead of typical divs. You'll be creating a dynamic map that retrieves the coordinates of different critter types when you select them from the drop-down, and displays them on a map (see images below). As before, we'll be faking the coordinate database with static JSON files.

![](https://faculty.utrgv.edu/emmett.tomai/courses/3342/assignments/ajax/critter_map.png)



The starter files for the project are in this repository.

- Entry point: critters.html
- Other files: critters.css, critters.js, data0.json, data1.json, data2.json

Note that the .css file already has styling for the main map, and the .js file already has an array of urls for the images. Here's how I suggest you approach the problem of recreating that map:

- Figure out how to insert an image onto the page from javascript. I'd recommend creating an img element and setting the *src* attribute, then inserting it.
- Resize the picture you're inserting, and try put it in different places. css positioning will be involved. Modify the **top** and **left** CSS styles to position the image.
- Trigger on select to make an ajax call to get data0.json, data1.json or data2.json. The data is an array of x,y coordinates, each describing where on the page to put a critter. Make sure you get back good data.
- **Data generality!** Note that the select box in the HTML file has `value` attributes for each `option` which are the numbers 0, 1, 2. Imagine that those numbers are IDs pulled from the database that match the critter types, so if there were also types 3, 4, and 5, your code would work without change.
- Loop over the data to put multiple critter images on the screen. Don't forget to clear out the old images each time you select a new critter!
- If the critters don't appear in quite the same spots, that's fine, we're not picky. Just pay attention if the positioning might indicate some kind of problem with processing the coordinates or inserting the images into the page.