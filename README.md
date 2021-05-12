# Orbital Witness Technical Test

This document contains instructions for candidates to follow as part of the Orbital Witness Technical Assessment. We look forward to your submission.

# Objective
At Orbital Witness, we deal with a variety of data. One of them is data on titles from the Land Registry. In this assessment, we have provided an analogue of what we usually deal with on a day-to-day basis.

## User Story
As a User, I want to browse through an extensive list of titles efficiently, so I can look at its details and favourite them.

# Instructions
To complete the task, you need to create an app based on [these wireframes](https://github.com/orbitalwitness/tech-test/tree/main/wireframes).

## Functionality
App fetches [the JSON data about titles we’ve provided to you](https://github.com/orbitalwitness/tech-test/tree/main/data). It’s formatted like:

```
[
    {
        "id":"0",
        "titleNumber":"MYBKZ10625",
        "titleClass":"Freehold",
        "isFavorite":true,
        "content":"Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean convallis lectus velit, ac mollis lorem fringilla ac. In consequat molestie dui, et pellentesque nisl convallis at. Curabitur dictum lacinia justo, pulvinar pharetra purus ru"
    },
    {
        "id":"1",
        "titleNumber":"GP51",
        "titleClass":"Leasehold",
        "isFavorite":true,
        "content":"Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean convallis lectus velit, ac mollis lorem fringilla ac. In consequa"
    },
]
```

It has 2 pages: titles, and favorites. Each of them is selectable through sidebar navigation.

## Titles page

<details>
<summary>Show wireframes</summary>
<p>

#### List of titles and title details

![Titles page](wireframes/Titles%20page.png)

#### Dropdown filter

![Titles page - dropdown](wireframes/Titles%20page%20-%20dropdown.png)

</p>
</details>

 - This page contains a table of titles. It must be paginated; you need to display 20 titles on every page. **Be careful with the URL**; I want to stay on page 6 if I refresh the page!
 - Hover over a row makes is gray, and click on it opens the titles details to the right. Selected title’s row should stay gray. **This is a thing only on desktop**; on mobile, you should just add a title to the favorites.
 - Click on the star in title details makes the title a favorite (and makes the star purple).
 - On click of the table header cell “Class of title”, a dropdown opens with two checkboxes. They should filter Freehold/Leasehold classes.
 - On click of the table header cell “Title number”, you should sort the titles ascending (A-Z). Another click sorts it descending. 3rd click sorts it initially.

## Favorites page

<details>
<summary>Show wireframes</summary>
<p>

![Favourites page](wireframes/Favourites%20page.png)

</p>
</details>


- This page contains all the titles which are favorites. Click on any just removes them from the list.

## What you should focus on
- Obviously, this needs to be done with React (and Typescript). Use the best patterns you know here, and don’t hack anything just because it’s a small app. Imagine that you’re creating a new feature for your commercial project. Using stuff like Router, Store, etc. is preferred.
- Let us know in the README how we can start the app.
- Margins and paddings don’t have to be the same as in wireframes. However, they should all be divisible by 4. Use your common sense when deciding about their exact values across the app. Same goes with the font sizes.
- CLEAN CODE! **You don’t need to implement everything, but whatever you do has to be your best offer**.
- Responsive design! Care about widths from 375px to 1280px. It should look appropriately on all of those widths.
- We love tests as well :)
- Please don’t use any UI frameworks (like material-UI); build everything with the pure HTML and CSS/SCSS/CSS-in-JS, whatever suits you the best.
- We don’t care about the icons, but they should be consistent across the app. Maybe https://fonts.google.com/icons?selected=Material+Icons? Again, whatever source you have is fine.
