## Trend Blogger Website Documentation

This documentation provides a comprehensive overview of the files and code used to create the Trend Blogger website.

### 1.  `index.html` - The Main HTML Structure

*   **DOCTYPE declaration:** Defines the document as HTML5.
*   **HTML `<html>` element:** Contains the entire structure of the webpage, including the head and body sections.
*   **Head `<head>` section:**
    *   **Meta tags:**
        *   `<meta charset="UTF-8">`: Sets the character encoding to UTF-8 for proper display of various characters.
        *   `<meta http-equiv="X-UA-Compatible" content="IE=edge">`: Ensures compatibility with older versions of Internet Explorer.
        *   `<meta name="viewport" content="width=device-width, initial-scale=1.0">`: Sets the viewport for responsive design on different devices.
    *   **Title `<title>` element:** Defines the title of the webpage displayed in the browser tab.
    *   **External CSS link:**
        *   `<link href='https://unpkg.com/boxicons@2.1.4/css/boxicons.min.css' rel='stylesheet'>`: Links the Boxicons icon library for using icons.
        *   `<link rel="stylesheet" href="styles.css">`: Links the custom CSS file to style the webpage.
*   **Body `<body>` section:**
    *   **Header `header` element:**
        *   **Navigation `nav` element:** Contains the logo and sign-up button.
    *   **Home `section` element:**
        *   **Home text `home-text` element:**  Displays the headline and subtitle.
    *   **About `section` element:**
        *   **Content `contentBx` element:**  Provides the about section's content.
        *   **Image `imgBx` element:** Displays the image related to the about section.
    *   **Post filter `post-filter` element:**
        *   **Filter items `filter-item`:**  Provides filter options for posts based on categories (All, Tech, Food, News).
    *   **Post `post` element:** Contains the blog posts.
        *   **Post boxes `post-box`:**  Individual containers for each post.
            *   **Post image `post-img`:**  Displays the image for the post.
            *   **Category `category`:**  Shows the post's category (Tech, Food, News).
            *   **Post title `post-title`:**  Displays the title of the post.
            *   **Post date `post-date`:**  Displays the date of the post.
            *   **Post description `post-description`:**  Provides a brief summary of the post.
            *   **Profile `profile`:**  Displays the author's image and name.
    *   **Footer `footer` element:**
        *   **Footer container `footer-container`:**  Contains sections for About Us, Quick Links, and Contact Info.
        *   **Sections `sec`:** Individual sections within the footer container.
            *   **About Us `aboutus`:**  Displays information about the website.
            *   **Quick Links `quicklinks`:**  Provides links to important pages (Home, About).
            *   **Contact Info `contactBx`:**  Displays contact details (address and email).
    *   **External JavaScript links:**
        *   `<script src="https://cdnjs.cloudflare.com/ajax/libs/jquery/3.6.1/jquery.min.js"></script>`:  Links the jQuery library for JavaScript interaction.
        *   `<script src="script.js"></script>`: Links the custom JavaScript file for dynamic functionality.

### 2.  `styles.css` - The Styling Code

*   **Font import:**
    *   `@import url('https://fonts.googleapis.com/css2?family=Poppins:ital,wght@0,600;0,700;1,400&display=swap');`: Imports the 'Poppins' font from Google Fonts.
*   **Global styles:**  Applies basic styling to all elements, including:
    *   Font family:  Sets the default font to 'Poppins'.
    *   Margin and padding:  Resets default margin and padding.
    *   Scroll behavior:  Enables smooth scrolling.
    *   Scroll padding:  Adds padding at the top for better scrolling experience.
    *   Box sizing:  Sets box-sizing to border-box for easier layout.
*   **Root variables:**  Defines custom CSS variables for colors, fonts, and other elements.
*   **Selection styles:**  Styles the selection highlight.
*   **Link styles:**  Removes text decoration and sets default color for links.
*   **List item styles:**  Removes default bullet points from list items.
*   **Image styles:**  Sets the image width to 100%.
*   **Section styles:**  Adds padding to section elements.
*   **Container styles:**  Sets a maximum width for the container and centers it horizontally.
*   **Header styles:**  Styles the header element with a fixed position, background color, and shadow when scrolling.
*   **Navigation styles:**  Styles the navigation bar with flexbox for alignment.
*   **Logo styles:**  Styles the logo text with font size, weight, and color.
*   **Login button styles:**  Styles the login button with padding, background color, border-radius, and text styles.
*   **Home section styles:**  Styles the home section with background image, grid layout, and text color.
*   **About section styles:**  Styles the about section with flexbox layout, image placement, and text styles.
*   **Button styles:**  Styles the 'Read More' button with background color, border, and hover effects.
*   **Post filter styles:**  Styles the post filter with flexbox for alignment and hover effects.
*   **Post styles:**  Styles the post section with grid layout, gap, and individual post container styling.
*   **Post box styles:**  Styles each post container with background color, box shadow, padding, and border-radius.
*   **Post image styles:**  Styles the post image with width, height, object fit, and border-radius.
*   **Category styles:**  Styles the category text with font size, weight, and color.
*   **Post title styles:**  Styles the post title with font size, weight, color, and line-clamp for truncation.
*   **Post date styles:**  Styles the post date with font size, weight, and text transformation.
*   **Post description styles:**  Styles the post description with font size, line height, and line-clamp for truncation.
*   **Profile styles:**  Styles the author's profile with flexbox alignment, image styling, and text styles.
*   **Footer styles:**  Styles the footer element with background color, padding, and flexbox layout.
*   **Footer container styles:**  Styles the footer container with flexbox layout for alignment.
*   **Section styles (footer):**  Styles the sections within the footer with margin, width, and title styles.
*   **Social media icon styles:**  Styles the social media icons with background color, hover effects, and icon sizes.
*   **Quick Links styles:**  Styles the quick links section with width and list item styling.
*   **Contact Info styles:**  Styles the contact information section with width, list item styling, and text styles.
*   **Media query styles:**  Applies different styling based on screen size for responsive design.

### 3.  `script.js` - The JavaScript Code

*   **Navigation background toggle:**
    *   `header.classList.toggle("shadow", window.scrollY > 0);`:  Adds a class "shadow" to the header element when scrolling, creating a shadow effect.
*   **Post filter functionality:**
    *   `$(".filter-item").click(function () { ... });`:  Handles click events on the filter items.
    *   `const value = $(this).attr("data-filter");`:  Gets the filter value (All, Tech, Food, News) from the clicked item.
    *   `$(".post-box").show("1000");`: Shows all posts if the filter value is "all".
    *   `$(".post-box").not("." + value).hide(1000);`: Hides posts that don't match the filter value.
    *   `$(".post-box").filter("." + value).show("1000");`:  Shows posts that match the filter value.
    *   `$(this).addClass("active-filter").siblings().removeClass("active-filter");`: Adds the "active-filter" class to the clicked item and removes it from other filter items.

## Summary

The Trend Blogger website uses HTML, CSS, and JavaScript to create a visually appealing and interactive blog website. The HTML provides the structure, the CSS styles the elements, and the JavaScript adds dynamic functionality, such as the post filtering feature. 
