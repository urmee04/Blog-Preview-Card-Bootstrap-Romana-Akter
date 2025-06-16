### Lab 3.3: Developing with Bootstrap

#### Second Challenge – Blog Preview Card

This project is a refactored version of my original Blog Review Card built with custom CSS. As part of a Lab- the goal was to convert this component to use **Bootstrap utility classes and components** to improve consistency, responsiveness, and maintainability across projects.


##### Objectives

- Refactor an existing project using Bootstrap’s utility classes.
- Use Bootstrap components to replace custom-styled elements.
- Apply Bootstrap’s grid system for responsive layouts.
- Demonstrate the ability to leverage Bootstrap documentation for efficient development.

##### Features

- Responsive layout for mobile and desktop.
- Semantic HTML structure using `<article>`, `<header>`, `<main>`, and `<footer>`.
- Hover effect on the card and card title with smooth transitions.
- Focus accessibility on interactive elements using `:focus` styles.
- CSS custom properties (`:root`) for easy color management.

##### Technologies Used

- Semantic HTML5
- Bootstrap 5.3.3
- Google Fonts (Figtree: weights 500, 800)

##### How to Use

1. Clone the repository or download the ZIP.
2. Be sure to maintain the folder structure (`assets/images/`).
3. Open `card.html` in your browser to view the card.

- git clone https://github.com/urmee04/Blog-Preview-Card-Romana-Akter
- cd blog-review-card-main
- cd card.html
- open card.html

#### Design Specifications
- Mobile width: 375px

- Desktop width: 1440px

- Font family: Figtree

- Font weights: 500, 800

###### Colors:

- Yellow: hsl(47, 88%, 63%)

- White: hsl(0, 0%, 100%)

- Grey: hsl(0, 0%, 50%)

- Black: hsl(0, 0%, 7%)

##### Accessibility
- Title made focusable via tabindex="0".
- Focus outline included for keyboard users.
- Images have descriptive alt attributes.

##### Reflections

1. What challenges did you face when refactoring your code to use Bootstrap?
Challenge:
One of the main challenges was translating precise custom designs into Bootstrap utility classes without writing custom CSS. For instance, replicating the exact spacing, font weights, and border effects required experimentation with Bootstrap’s padding (p-*), margin (mb-*, mt-*), and shadow classes.

Example:
In the original CSS, I had:

.card {
  padding: 1.5rem;
  box-shadow: 8px 8px 0 0 var(--black);
}
In Bootstrap, I approximated it with:

<div class="card p-4 shadow" style="box-shadow: 8px 8px 0 0 #000;">
However, box-shadow like this isn’t available directly via Bootstrap, so I had to retain inline custom style. That balance between Bootstrap and minimal custom styling was tricky.

2. How did using Bootstrap utility classes and components simplify your styling process?
Simplification:
Bootstrap utility classes allowed for rapid layout and alignment without writing any new CSS. This meant I could use predefined classes for common layout tasks instead of repeating CSS rules.

Example:

Instead of this custom CSS:

body {
  display: flex;
  justify-content: center;
  align-items: center;
}
I used Bootstrap classes:

<body class="d-flex justify-content-center align-items-center min-vh-100 bg-warning">
Also, for alignment and spacing:

<h1 class="fs-4 fw-bold mb-3">HTML & CSS foundations</h1>
replaced several lines of custom font and spacing rules.

Result:
Much faster development, cleaner HTML, and fewer lines of CSS.

3. In what scenarios might you choose not to use Bootstrap and write custom CSS instead?
**Scenarios to avoid Bootstrap:**

- When working on a highly customized design system that doesn’t align with Bootstrap’s opinionated styles.

- If performance is critical and we want to avoid the overhead of the full Bootstrap bundle.

- For micro-interactions or fine-tuned animations that Bootstrap doesn't support out-of-the-box.

Example:
In my original project, I had this neat hover effect:

.card:hover {
  transform: translate(-2px, -2px);
  box-shadow: 12px 12px 0 0 var(--black);
}
This subtle "card pop" effect is hard to recreate with Bootstrap alone, so I might choose to keep custom CSS in this case.















