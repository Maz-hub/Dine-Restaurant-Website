# Frontend Mentor - Dine Website Challenge

![Design preview for the Dine Website Challenge coding challenge](./preview.jpg)

This is a two-page responsive website built as a Frontend Mentor challenge.

## ✨ Features

- Mobile, tablet, and desktop layout
- Tabbed sections for events (Family Gatherings, Special Events, Social Events)
- Booking form with client-side JavaScript validation
- Accessible, semantic HTML
- Clean and organized CSS using modern layering practices

## 🧠 Skills Practiced

- CSS layout and responsiveness
- JavaScript form validation
- DOM manipulation and basic interactivity
- Organizing styles using `@layer` and CSS custom properties
- Version control with Git and GitHub

## 🚀 Live Demo

🔗 [View site on GitHub Pages](#)

## The challenge

Your challenge is to build out this multi-page website and get it looking as close to the design as possible.

You can use any tools you like to help you complete the challenge. So if you've got something you'd like to practice, feel free to give it a go.

Your users should be able to:

- View the optimal layout for each page depending on their device's screen size
- See hover states for all interactive elements throughout the site
- See the correct content for the Family Gatherings, Special Events, and Social Events section when the user clicks each tab
- Receive an error message when the booking form is submitted if:
  - The `Name` or `Email Address` fields are empty should show "This field is required"
  - The `Email Address` is not formatted correctly should show "Please use a valid email address"
  - Any of the `Pick a date` or `Pick a time` fields are empty should show "This field is incomplete"

## Notes & Features

### 🧱 About @layer in CSS

This project uses the modern CSS @layer feature to organize styles more clearly and control how they cascade.

```css
@layer color, global, components;

@layer color {
  :root {
    --c-Beaver: #9e7f66;
    --c-Cod-Gray: #111111;
}

@layer global {
  h1,
  h2,
  h3 {
      margin: 0;
    }
}
```

✅ What @layer does:

- Helps group styles into layers (like folders inside CSS)
- Makes CSS easier to read, maintain, and scale
- Lets the browser know the order of importance, so one style doesn't accidentally override another

> Instead of relying only on the order of CSS file, `@layer` gives more control over the cascade, especially in larger projects or when combining multiple style sources.

### 🔤 Self-hosting Google Fonts with Webfonts Helper

Instead of linking to Google Fonts using a remote URL, this project uses Google Webfonts Helper to download and self-host font files locally.

✅ Why I did this:

- Faster loading: Fonts are served directly from my own site
- More privacy-friendly: No external requests to Google Fonts
- Better control: I can choose exactly which font weights and subsets I need

🛠 How I did it:

1. Went to [Google Webfonts Helper](https://gwfh.mranftl.com/fonts)
2. Selected the font and styles used in the design
3. Downloaded the .woff / .woff2 files and placed them in a fonts folder
4. Copied the generated @font-face CSS into my main stylesheet
5. Used the font in my project like any other custom font

> This method improves performance and aligns with best practices for font loading.
