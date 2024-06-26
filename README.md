# Visit here:
<a href="https://music-academy-gamma.vercel.app/" target="_blank">Visit this project website</a>


# Intro to Next JS:

    Next.js is a popular open-source framework built on top of React.js for building
    modern web applications. It is primarily used for server-side rendering (SSR),
    static site generation (SSG), and client-side rendering (CSR) of React
    applications. Next.js simplifies the development of React applications by
    providing various features and optimizations out of the box.

## Section 1: Introduction, App Structure and Routing Basics

### Creating Next App:

    ```jsx
        npx create-next-app@latest
    ```
    After this we select all we need.
      - TypeScript
      - ESLint
      - Tailwind CSS
      - 'src' dierctory
      - App Router
      - Don't customize import alias

### App Structure:

    1. Layout:
        A Wrapper.
        Children imported from page.tsx

    2. Page:
        For Content.
        Has to be named page.tsx

### Routing:

    - Routing is super easy in next.
    - Create a new folder with the route name. The file inside this route name must
      be page.tsx. For example, I created a folder named "tab" with a page.tsx fill
      in it. Then 'localhost3000/tab' is how I would access the tab page.
    - Folder name can be anything but the file name has to be page.tsx.

### Layout:

    - In main layout, just above the children I added a 'NavBar'. Now this NavBar
      being in the main Layout will appear in all routes. For example, on the main
      page '/' the NavBar is present; on the tab page 'localhost3000/tab' the
      NavBar is again present.
    - So the layout is based on the name of the folder. We can add layout file inside
      the, say 'tab' folder. Then have another NavBar just above the {children}.
      When we route to 'localhost3000/tab' the main NavBar from main layout is
      present as well as the 'Inner NavBar' from the layout in 'tab' folder is also
      present.
    - We can have multiple layouts just like this, like a nested layout. Further,
      we can add more folder inside of 'tab' folder and add page and layout inside of
      it.

## Section 2: Navbar

### Components:

    - We can use a third party open source website for components.
    - Go to Aceternity UI and get the desired component.
    - Follow the steps as instructed.
    - Now how to use the component? Say we got the Navbar component, now we want to
      use it on our UI. Be sure to put 'use client' on top of our component file. Why?
      We need to use some React hooks in our component file. This will make this
      particular component a client component. As discussed, Next JS is a fullstack
      framework, all our React hooks are on the client side.
    - After using a component from Aceternity, we tweek into it and configure it
      ourselves. Like for example, we want Home and Contact Us with no children, only
      have a drop down menu when there are children.

## Section 3: Hero Section

    - Challenges:
      Moving Border and Spotlight effect in background.
    - Create a HeroSection component. Then we need it in page.tsx. Why?
      HeroSection should be displayed as a children, we don't want hero section
      to appear everywhere like Navbar whenever we scroll up or down.
    - Using some css inside a div we style the text. 
    - How do I use spotlight in the background? Go to Aceternity > Spotlight. 
      Then its basic copy paste as instructed.
    - Similarly, get the moving border component. Copy paste as instructed.

## Section 4: Card Section and Intro to Typescript:
    - 3 sections in this. Title, cards and button.
    - Typescript:
      - We need to get the data from a JSON file.
      - We have an array named courses in which data objects are stored.
      - To do so, we created a new data type named Courses using typescript. Why?
      - Check the FeaturedCourses.tsx file.
      - Then through simple JS we get the data from the data.
```tsx
// create own data type:
interface Course {
  id: number,
    title: string,
    slug: string,
    description: string,
    price: number,
    instructor: string,
    isFeatured: boolean,
}
```

## Section 5: Testimonial cards and Grid Background:
    - Get the infinite moving cards from Accertinity.
    - For Grid / Dot Background in Accertinity: 
      - We see there's no import, it's a Tailwind property. 
      - Need to import stuff into the tailwind config file.
      - See the code below on how to use this background.

```tsx
// for grid --> The /[0.2] is the opacity of the grid / dots
<div classname="dark:bg-black dark:bg-grid-white/[0.2]">
  Content
</div>
// for dot
<div classname="dark:bg-black dark:bg-dot-white/[0.2]">
  Content
</div>
```

## Library Used => Accertinity

## More Libraries to explore: ShadCN and DaisyUI