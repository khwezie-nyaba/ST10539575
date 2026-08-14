LokusaTreats Website
A multi-page website for LokusaTreats, a boutique confectionery brand based in Cape Town, South Africa, offering handcrafted cupcakes, cookies, chocolates, and celebration hampers.
Overview
LokusaTreats began in 2015 as a market stall and has grown into a licensed boutique bakery. This site serves as the brand's online storefront, showcasing best-selling products, custom cake enquiries, corporate/bulk ordering, a gallery, blog, and contact details.
Pages


File
Purpose
index.html
Home page — hero banner, value props, featured treats, brand story preview, testimonials, promo, Instagram feed, newsletter sign-up
about.html
Full brand story
shop.html
Full product menu
product-detail.html
Individual product page (expects a ?id= query parameter, e.g. cupcake-box-6)
custom-orders.html
Custom cake / celebration order enquiries
corporate.html
Corporate & bulk order info
gallery.html
Photo gallery
blog.html
Blog listing
contact.html
Contact details
cart.html
Shopping cart
privacy-policy.html
Privacy policy
terms.html
Terms & conditions
Project Structure
LokusaTreats/
├── index.html
├── about.html
├── shop.html
├── product-detail.html
├── custom-orders.html
├── corporate.html
├── gallery.html
├── blog.html
├── contact.html
├── cart.html
├── privacy-policy.html
├── terms.html
├── css/
│   └── style.css
├── js/
│   ├── products.js
│   ├── cart.js
│   └── main.js
└── assets/
    ├── images/
    │   ├── hero-treats.jpg
    │   ├── about-kitchen.jpg
    │   ├── logo.svg
    │   └── insta-1.jpg … insta-6.jpg
    └── icons/
        ├── icon-handmade.svg
        ├── icon-ingredients.svg
        └── icon-delivery.svg
Setup
Clone or download the project folder.
Make sure the assets/ and css/ folders sit alongside the HTML files as shown above.
Open index.html in a browser, or serve the folder with a local dev server (e.g. VS Code's Live Server extension) for the best results.
No build step or package manager is required — this is a static HTML/CSS/JS site.
⚠️ Known Issues / To Fix
Broken image paths: Several <img> tags reference absolute local file paths from a single machine, e.g.:
<img src="C:\Users\Student\Documents\LokusaTreats\Images\Cupcakes.jpg">
These will only work on that one computer and must be replaced with relative paths into assets/images/ (matching the pattern used elsewhere on the page, like assets/images/hero-treats.jpg) before the site will display correctly for anyone else or when deployed.
Oversized image dimensions on small files: Several images are hard-coded to width="250" height="150", including the logo and hero image — worth double-checking these against the actual intended display size.
Placeholder links: Social icons, the search/account icons in the header, and the Instagram feed thumbnails currently point to # and will need real URLs.
Newsletter form: newsletter-form posts to action="#" — needs a real endpoint or JS handler.
Footer year: <span id="year"></span> is empty and expects main.js to populate the current year via JavaScript.
Scripts
js/products.js — product data / rendering logic
js/cart.js — cart functionality (add to cart, cart count)
js/main.js — general site behavior (e.g. footer year, nav toggle)
Tech Stack
HTML5
CSS3 (css/style.css)
Vanilla JavaScript
License
© LokusaTreats. All rights reserved.
