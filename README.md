# Elm-UI unofficial FAQs


# How can I style the scrollbars?

Scrollbar styling isn't well supported in all browsers so it isn't possible to do it directly. You can draw your scrollbar on the top of the actual scrollbar to fake it though/

Maybe you want to use `Element.clip`? It depends on what you want to happen to stuff that doesn't fit.


# Does Elm-UI support Dropdowns?

There are two packages, the first one is better maintained by a company invested in Elm (but it's also more clunky and odd to use), the latter is a community package maintained by 1 individual with a much simpler API. Your pick:

https://package.elm-lang.org/packages/PaackEng/elm-ui-dropdown/latest

https://package.elm-lang.org/packages/russelldavies/elm-ui-searchbox/latest/

The latter doesn't behave exactly like a dropdown until the user begins searching, so that may be a deal-breaker depending on your UI requirements!

# Is there any solution for missing `Font.cursive` or other font families?

`cursive` and `fantasy` aren't available in elm-ui . You'll have to construct your own CSS rule if you want to use them. For a consistent design, you should just pick a specific font stack. There's an argument for using built-in fonts for faster loading.  system-ui is interesting, though some gotchas are pretty subtle: https://infinnie.github.io/blog/2017/systemui.html

# This HTML block added with `Element.HTML` does not align properly

Wrap it in an `Element.el`.
