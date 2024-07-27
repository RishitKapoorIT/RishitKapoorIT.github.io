# Personal Portfolio Template

## Demo
View a live demo of [Rishit Kapoor's Portfolio Template](https://example-portfolio-template.netlify.app/).

## Installation

### Step 1: Environment Setup
```bash
winget install Schniz.fnm
fnm use --install-if-missing 20
node -v # should print `v20.16.0`
npm -v # should print `10.8.1`

Step 2: Install Tailwind CSS
 npm install -D tailwindcss
npx tailwindcss init

Step 3: Configure 'tailwind.config.js'
/** @type {import('tailwindcss').Config} */
module.exports = {
  content: ["./src/**/*.{html,js}"],
  theme: {
    extend: {},
  },
  plugins: [],
}

Step 5: Run Tailwind CSS
npx tailwindcss -i ./src/styles.css -o ./src/output.css --watch

Step 6: Basic HTML File
<!doctype html>
<html>
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <link href="./output.css" rel="stylesheet">
</head>
<body>
  <h1 class="text-3xl font-bold underline">
    Hello world!
  </h1>
</body>
</html>

Step 7: Install DaisyUI
npm i -D daisyui@latest

Step 8: Update 'tailwind.config.js' to Include DaisyUI
/** @type {import('tailwindcss').Config} */
module.exports = {
  content: ["./src/**/*.{html,js}"],
  theme: {
    extend: {},
  },
  plugins: [
    require('daisyui'),
  ],
}

Project Structure
├── src/
│   ├── components/
│   │   ├── cv/
│   │   │   ├── TimeLine
│   │   ├── BaseHead.astro
│   │   ├── Card.astro
│   │   ├── Footer.astro
│   │   ├── Header.astro
│   │   └── HorizontalCard.astro
│   │   └── SideBar.astro
│   │   └── SideBarMenu.astro
│   │   └── SideBarFooter.astro
│   ├── content/
│   │   ├── blog/
│   │   │   ├── post1.md
│   │   │   ├── post2.md
│   │   │   └── post3.md
│   │   ├── store/
│   │   │   ├── item1.md
│   │   │   ├── item2.md
│   ├── layouts/
│   │   └── BaseLayout.astro
│   │   └── PostLayout.astro
│   └── pages/
│   │   ├── blog/
│   │   │   ├── [...page].astro
│   │   │   ├── [slug].astro
│   │   └── cv.astro
│   │   └── index.astro
│   │   └── projects.astro
│   │   └── rss.xml.js
│   ├── styles/
│   │   └── global.css
│   └── config.ts
├── public/
│   ├── favicon.svg
│   └── profile.webp
│   └── social_img.webp
├── astro.config.mjs
├── tailwind.config.cjs
├── package.json
└── tsconfig.json

Site Configuration
You can change global site configuration in the /src/config.ts file:

SITE_TITLE: Default pages title.
SITE_DESCRIPTION: Default pages description.
GENERATE_SLUG_FROM_TITLE: By default, it generates the blog slug pages based on the article name. Set this to false to use the Astro file base (compatible with older versions).
TRANSITION_API: Enable or disable transition API.
Components Usage
Layout Components
The BaseHead, Footer, Header, and SideBar components are included in the layout system. Edit these components to change the website content.

SideBar
In the Sidebar, you can change your profile picture, links to all your website pages, and your social icons. You can change your avatar shape using mask classes. The social icons are from the BoxIcons pack. You can replace the icons in the SideBarFooter component. To add a new page in the sidebar, go to the SideBarMenu component.
<li><a class="py-3 text-base" id="home" href="/">Home</a></li>

Note: To change the sidebar menu's active item, set the prop sideBarActiveItemID in the BaseLayout component of your new page and add that ID to the link in the SideBarMenu.

TimeLine
The timeline components are used to confirm the CV.
<div class="time-line-container">
  <TimeLineElement title="Element Title" subtitle="Subtitle">
    Content that can contain
    <div>divs</div>
    and <span>anything else you want</span>.
  </TimeLineElement>
  ...
</div>


Card & HorizontalCard
The cards are primarily used for the Project and Blog components, including a picture, title, and description.
<HorizontalCard title="Card Title" img="img_url" desc="Description" url="Link URL" target="Optional link target (_blank default)" badge="Optional badge" tags={['Array','of','tags']} />

HorizontalCard Shop Item
This component is included in the Store layout of the template. Use the following props:
<HorizontalShopItem
  title="Item Title"
  img="img_url"
  desc="Item description"
  pricing="current_price"
  oldPricing="old_price"
  checkoutUrl="external store checkout url"
  badge="Optional badge"
  url="item details url"
  custom_link="Custom link url"
  custom_link_label="Custom link btn label"
  target="Optional link target (_self default)"
/>

Adding a Custom Component
To add a custom component, create a .astro file in the components folder under the src folder. Components must follow this template:
---
<!-- Component Script (JavaScript) -->
---
<!-- Component Template (HTML + JS Expressions) -->
For more details, see the Astro components documentation.

Layouts
Include BaseLayout in each page you add and PostLayout to your post pages. The BaseLayout defines a general template for each new webpage. It imports constants SITE_TITLE and SITE_DESCRIPTION which can be modified in the ../config folder.

Content
Add a content collection in the /content/ folder. You will need to add it in config.ts.

Blog
Add your .md blog post in the /content/blog/ folder.

Post Format
Add the following code at the top of each post file:
---
title: "Post Title"
description: "Description"
pubDate: "Post date format (Sep 10 2022)"
heroImage: "Post Hero Image URL"
---

Pages
Blog
The blog uses Astro's content collection to query post's .md.

[page].astro
The [page].astro route works with the paginated post list. Change the number of items listed for each page and the pagination button labels here.

[slug].astro
The [slug].astro route is the base for every blog post. Customize the page layout or behavior. By default, it uses content/blog for content collection and PostLayout as layout.

Shop
Add your .md item in the /pages/shop/ folder.

[page].astro
The [page].astro route works with the paginated item list. Change the number of items listed for each page and the pagination button labels here. The shop will render all .md files inside this folder.

Item Format
Add the following code at the top of each item file:
---
title: "Demo Item 1"
description: "Item description"
heroImage: "Item img URL"
details: true # show or hide details btn
custom_link_label: "Custom btn link label"
custom_link: "Custom btn link"
pubDate: "Sep 15 2022"
pricing: "$15"
oldPricing: "$25.5"
badge: "Featured"
checkoutUrl: "https://checkouturl.com/"
---

Static Pages
The other pages included in the template are static pages. The index page belongs to the root page. Add your pages directly in the /pages folder and then add a link to those pages in the sidebar component.

Theming
To change the template theme, change the data-theme attribute of the <html> tag in the BaseLayout.astro file. Choose among 30 themes available or create your custom theme. See themes available here.

Sitemap
The Sitemap is generated automatically when you build your website in the root of the domain. Update the robots.txt file in the public folder with your site name URL for the Sitemap.

Deploy
You can deploy your site on your favorite static hosting service such as Vercel, Netlify, GitHub Pages, etc. Configuration for deployment varies depending on the platform. See the official Astro information to deploy your website.

Note: The Blog pagination of this template is implemented using dynamic route parameters in its filename and is incompatible with SSR deploy configs. Use the default static deploy options for your deployments.

This separation should help in maintaining clear and organized files for your project.

