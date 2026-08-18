# Flexbox vs CSS Grid

## Project Overview

This project demonstrates the same 3-column pricing layout built using two different CSS layout systems: **Flexbox** and **CSS Grid**.

The layout includes a header, three pricing cards, and a footer. Both versions are responsive and stack into a single column when the screen width is below 600px.

## Flexbox Version

The Flexbox version uses:

```css
display: flex;
```

and:

```css
flex: 1;
```

Flexbox makes it easy to arrange the three pricing cards horizontally and distribute the available space evenly.

### Advantages

* Simple for one-dimensional layouts
* Easy to align and distribute elements
* Useful for rows or columns
* Good for smaller component layouts

### Disadvantages

* Less direct control over both rows and columns
* More difficult for complex two-dimensional layouts

## CSS Grid Version

The Grid version uses:

```css
display: grid;
```

and:

```css
grid-template-columns: repeat(3, 1fr);
```

Grid allows the three columns to be explicitly defined.

### Advantages

* Excellent for two-dimensional layouts
* Easy to control rows and columns
* Makes complex page structures easier to manage
* Provides precise control over spacing and positioning

### Disadvantages

* Can be more detailed than Flexbox for simple layouts
* May be unnecessary for basic one-dimensional arrangements

## Comparison

For this pricing layout, **Flexbox was easier for arranging the cards in a single horizontal row**. Using `display: flex`, `gap`, and `flex: 1` made the layout straightforward.

**CSS Grid provided more explicit control over the three columns**. The `grid-template-columns` property clearly defines the structure of the pricing section.

Overall, Flexbox is more suitable when elements mainly need to be arranged in one direction, while CSS Grid is better when a design requires control over both rows and columns.

## Responsive Design

Both versions use a media query at **600px**:

```css
@media (max-width: 600px) {
    ...
}
```

Below 600px, the three pricing cards change from a horizontal 3-column layout into a single vertical column.

## Conclusion

Both Flexbox and CSS Grid can create responsive layouts effectively. This project helped demonstrate that the choice between them depends on the structure of the layout.

**Flexbox → One-dimensional layouts**

**CSS Grid → Two-dimensional layouts**
