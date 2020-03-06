# AdvancedCss

## Contents

01. Sass
02. Responsive grid implementation.
03. Sass 7-1 Architecture.
04. Icon font usage.
05. CSS properties.

# Sass.

## Sass Import

@import

## Sass Partials

01. Starts with _
02. While import no prefix _ and no extension

## Sass variable 

01. $variableName
02. Inside css calc #{variableDeclaration})

## Responsive Design

### DESKTOP first.

**Media queries based on max-width.**

### MOBILE first

**Media queries based on min-width.**

01. Media queries doesn't add any specificity.

02. Breakpoint selections.

   - Select based on real world device popularity.
   
   - **Ignore devices all together and focus on content**

## 7-1 Architecture.

### Directory base

#### Animations

**suggested file name** _animations

#### Base

**suggested file name** _base

#### Typograpy

**suggested file name** _typograpy

#### Misc Utilities

**suggested file name** _utils

### Directory abstract

#### Variables
**suggested file name** _variables

#### Mixins

**suggested file name** _mixins

#### functions

**suggested file name** _functions

### component

### layout

### pages

### themes

### vendor

## Responsive design Essentials.

### Fluid Grids and Layouts

Three main categories.

01. Float Layouts.
02. FlexBox

   a. Unidirectional.

03. Css Grid.

   b. Bidirectional.

### Flexible and responsive images.

01. Image optimisation.

### Media Queries.

# Icon fonts.

Images does not scale well. Therefore vector icons fonts are better.
Svg is also an option.

## Font vs svg 

# CSS Properties

01. Perspective.

   -. Use moz prefix.

02. Background Clip

   - Webkit prefix.

03. Backface Visibility.
04. Background blend mode.

   - overflow hidden required if rouded coreners of parent and 
   image reaches the edges.

05. Clip Path
06. Box decoration break.
07. Perspective.
08. figure
09. shape-outside

   - element has to be floated.
   - with specified height and width.

10. Figure and figcaption.
11. filter.
12. video.
13. source
14. object-fit
15. Gradients.linear gradient mimicking clip-path
16. adjacent sibling,genric sibling,(both needs to be after the selected element) universal selector.
17. ::input-placeholder
18. :focus, :invalid, placeholder-shown, :checked. 
19. Custom radio button.
20. Checkbox hack.
21. Animation timing fns using bezier curves.
22. solid color gradients animations.
23. transform origin.
24. hypen
25. column-count
26. column-gap
27. column-rule
28. hyphen
29. :target

## Forward Content.

01. Animated buttons. No presentation to button presentation.
02. transform precedence.
03. Need for backface visibility.
04. src vs source.
05. Input element font family inheritence.
07. Visibility animation possibility.

