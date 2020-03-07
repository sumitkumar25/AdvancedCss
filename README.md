# AdvancedCss

## Contents

01. Sass
02. Responsive design without framework.
03. Sass 7-1 Architecture and BEM.
04. Icon font usage.
05. CSS properties.

# Sass

## Sass commonly used utilites

01. @import.
02. @include.  

    include mixins, partials.

03. @content  

    Pass a block of code to a mixin.

04. @supports  

    browser support checks.Used in implemention graceful degradation.

## Sass Partials

01. Starts with '_'.
02. While import no prefix _ and no extension.

## Sass variable 

01. $variableName
02. Inside css calc #{variableDeclaration})

# Responsive Design

### Fluid Grids and Layouts

Three main categories.

01. Float Layouts.

02. FlexBox (Unidirectional).

03. Css Grid.(Bidirectional).

### DESKTOP first.

Media queries based on max-width.

### MOBILE first

Media queries based on min-width.

### Font size (rem and em)

01. root defaults don't work in media queries conditionals..
02. **rem** and **em** derived from browser font-size and unaffected by root font size settings.

03. support for **rem** can be faulty use **em** for conditionals.
04. **rem** works fine for style rules.

### Media queries

01. Media queries doesn't add any specificity.Stylesheet order resolves conflicting rules.

02. Breakpoint selections.

   - Select based on real world device popularity.
   
   - **Ignore devices all together and focus on content**

03. Media Queries Usage. 
    01. Media query written for most of the style based on breakpoints.
    02. Mixin using @content projection.

    

``` css
    // following will result in no. of mixins === breakpoints.
    html {
        font-size: 62.5%;

        @include phone-view( {
                font-size:50%;
            }

        )
    }

    @mixin phone-view {
        @media (max-width:600px) {
            @content
        }
    }
```

04. Mixin with breakpoint as argument and using @if directive.

``` css
    /*
    following will result in 1 mixins and conditions equal to  
    breakpoints.
    */
    html {
        font-size: 62.5%;

        @include respond(phone) {
            font-size: 50%;
        }
    }

    @mixin respond($breakpoint) {
        @if $breakpoint==phone {
            @media (max-width:600px) {
                @content
            }
        }
    }
```

05. Order or styles **crucial** while using media queries.

### Images.

#### Adaptive images 
Images scaled using relative units.

#### Responsive images 

Using Responsive images involves use of different images based on different scenarios.

01. Resolution switching.  

    Serve a scaled down (low resolution image) for lower resolution views.

02. Density switching.   

    Opposite of resoultion switching.

03. Art direction.   

    Different image altogether for different screen sizes.

#### Responsive image usage in HTML

01. \<img> desity switch.   

    using sourceset attribute instead of src with **density descriptors**.

    

``` html
       <img srcset="url-1 1x, url-2 2x" alt="text">
```

02. \<picture> art direction. 

    media attribute allows for media queries in html.

    

``` html
    <picture>
        <source srcset="url-11 1x, url-21 2x" media="(max-wdith:37.2em)">
        <img srcset="url-1 1x, url-2 2x" alt="text">
    </picture>
```

03. \<img>  resolution switching using **width descriptors and sizes attribute**.  

``` html
       <img srcset="url-11 100w, url-21 200w" sizes="(max-width:900px) 20vw,(max-width:600px) 30vw,300px" alt="text">
```

#### Responsive image usage in CSS   

Use dpi based media queries combined with other conditions.

    

``` css
    @media (min-resolution:192dpi) {
        /* background change here */
    }
```

    

# 7-1 Architecture and BEM.

| Directory   | contains |
| :----------- | :----------- |
| base        |   animations, resets, typography, utils          |
| layout        |  header, footer, navigation, popup.|
| component   | forn, features        |
| abstract     | functions, mixins, variables        |
| pages        | application pages.|
| themes        |    ---         |
| vendor        |    --         |

# Icon fonts.

Images does not scale well. Therefore vector icons fonts are better.
Svg is also an option.

# CSS Properties

01. Perspective.  

    Use moz prefix.

02. Background Clip  

    Webkit prefix.

03. Backface Visibility.
04. Background blend mode.  

    overflow hidden required if rouded coreners of parent and 

   image reaches the edges.

05. Clip Path
06. Box decoration break.
07. Perspective.
08. figure
09. shape-outside  
    - element has to be floated.
    - specify height and width.

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
30. ::selection
30. background-filter.
___

