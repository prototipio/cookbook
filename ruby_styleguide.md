### Strip whitespaces
Callback approach is the best place for this. All your validations are run by callbacks so you can have data integrity. Stripping whitespace is something you want to run every single save as well for the same reason, so callbacks fit this really well.
[Everyone's Been Bitten Before - Whitespaces/Unwanted Characters in User Input](https://gorails.com/forum/everyone-s-been-bitten-before-whitespaces-unwanted-characters-in-user-input)


### Callbacks
Callbacks aren't always bad. When people give out the advice to "avoid callbacks" they're saying you shouldn't jump to that when you want to implement business logic. For example, **sending an email after registering with a callback isn't great because you can't turn it off.**
However, stripping whitespace is different because you'll always want that to run and you do want it closely coupled to your data since it's not business logic, it's for data integrity. Same reason why your validations always run on the validation callback, you always want them to run to keep the integrity of your data. 👍

From main article about strip whitespaces [Everyone's Been Bitten Before - Whitespaces/Unwanted Characters in User Input](https://gorails.com/forum/everyone-s-been-bitten-before-whitespaces-unwanted-characters-in-user-input)
