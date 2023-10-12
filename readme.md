In the _color.scss file I defined several variables, there are $font-stack: Arial, Helvetica, sans-serif; $light-color: #f4f4f4; $primary-color: #8b64ff; $secondary-color. orange; $main-color: #4292d2; $main-color: #4292d2; $main-color: #4292d2
I set the font-family to $font-stack and the background-color to $light-color in the body section of style.scss I applied the set- background function in the showcase-header and showcase-footer sections, using the $primary-color variable as a parameter. I have applied the set-background function to the showcase-main section and used the $main-color variable as an argument. In the btn-primary section of _buttons.scss I have set background-color with $primary-color.I have used $secondary-color in btn-secondary and button.

I used nesting in the showcase-header section of style.scss with the following code:
.showcase-header {
    @include set-background($primary-color);
    height: 600px;

    nav {
        display: flex;
        align-items: center;
        justify-content: space-between;
    }

    ul {
        display: flex;
        list-style-type: none;
    }

    li {
        padding: 15px;
    }

    &-content {
        height: 100%;
        display: flex;
        align-items: center;
        justify-content: center;

        img {
            width: 20%;
        }

        h1 {
            width: 50%;
        }

        h1 {
            font-size: 42px;
            line-height: 1.2;
        }

        p {
            margin: 20px 0;
        }

    }

}

.showcase-footer {
    @include set-background($primary-color);

    &-content {
        height: 100%;
        display: flex;
        flex-direction: column;

    }
}

.showcase-main {
    @include set-background($main-color);

    &-content {
        display: grid;
        grid-template-columns: 1fr 1fr;
    }
    img {
        width: 50%;
    }

}

I used interpolation in _utilities.scss with the following code:
$spaceamounts: (1, 2, 3);

@each $space in $spaceamounts{
    .my-#{$space}{
        margin: #{$space}rem;
    }
}

I used placeholder selectors in _buttons.scss with the following code:
%btn {
    display: inline-block;
    border-radius: 5px;
    padding: 8px 20px;
    margin: 3px;
    text-decoration: none;

    &:hover {
        transform: scale(0.98);
    }
}
And I apply placeholder in .btn-primary, .btn-secondary, and .button.

I used @mixin in _color.scss to set backgroud color.
I used @function in _color.scss to set text color. 
I also used @each in _utilities.scss to set margin.
I used @if, @else, and @return in the _color.scss.
I used built-in function "lighten" in _buttons.scss to set background
I used operators in style.scss I set 
img {
        width: 100% / 2;
    }
I used partials and imports in style.scss
