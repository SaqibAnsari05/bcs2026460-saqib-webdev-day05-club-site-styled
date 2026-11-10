
# Day 05 - Design Notes

## 1. Design Overview

The Campus Connect website uses a modern dark green theme with light green accents. The design focuses on readability, consistency and a clean student-friendly interface.

## 2. Color Palette

| Purpose | Color |
|---|---|
| Main Background | #101713 |
| Surface | #19231d |
| Light Surface | #222f27 |
| Primary Accent | #a3e635 |
| Secondary Accent | #84cc16 |
| Main Text | #f1f5f0 |
| Muted Text | #aab8ad |

## 3. Typography

- Heading Font: Manrope
- Body Font: DM Sans
- Base Font Size: 16px
- Responsive heading sizes use CSS clamp().

## 4. CSS Design Tokens

CSS custom properties are defined inside :root.

Examples:
- --color-bg
- --color-primary
- --color-text
- --space-sm
- --space-lg
- --radius-md

These variables help maintain consistent styling and make future changes easier.

## 5. CSS Selectors Used

- Element selectors: body, h1, p, a
- Class selectors: .container, .navbar, .card
- ID selector: #join-us
- Descendant selectors: .content-box p, .navbar .nav-links a
- Pseudo-classes: :hover and :focus
- Attribute selectors: input[type="checkbox"]

## 6. Class vs ID Specificity Experiment

A class selector and an ID selector were tested using browser Developer Tools.

Example:

.cascade-test {
    color: white;
}

#cascade-test {
    color: #a3e635;
}

HTML:

<div class="cascade-test" id="cascade-test">
    CSS Cascade Test
</div>

The ID selector has higher specificity than the class selector, so its color rule takes priority when both declarations have equal importance.

## 7. Responsive Design

Media queries are used at:
- 800px
- 550px

The card layout changes from three columns to two columns and then to one column on smaller screens.

The navigation also changes to a vertical layout on smaller screens.

## 8. Units Used

- rem for spacing, typography and sizing
- percentages for fluid container width
- clamp() for responsive typography
- px for borders and small fixed details

## 9. Debugging and Testing

The website was checked in the browser.

Testing checklist:
- CSS stylesheet loads on all pages.
- Navigation links open the correct pages.
- Buttons and forms are visually readable.
- Card layouts adapt to smaller screens.
- Text has sufficient contrast against the background.

## 10. Conclusion

The Day 05 assignment improves the original Campus Connect website using external CSS, reusable design tokens, selector specificity, typography, spacing and responsive layouts.
