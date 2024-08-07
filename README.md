## Facer Technical Assignment - Introduction

This exercise involves taking over an existing codebase that manages the inventory of a store selling watches, implementing new requirements, and delivering a maintainable version of it.

For this technical assignment, you are free to choose any language from the provided options. Currently, it's either Kotlin or Typescript. If you're applying for a frontend position, we encourage you to pick Typescript; if you're applying for an Android position, we encourage you to choose Kotlin. Each language contains a README file with some context on how to run the program provided. Feel free to fork this repository for your solution. Below you'll find the requirements for the exercise.

## Scenario Setup

Imagine we are a small watch shop in the mountains of Switzerland. We have a nice shop in one of the valleys, and we sell all kinds of products. Unfortunately, the climate isn't well suited for keeping watches in great condition. Due to this, our watches degrade in quality every day that we don't sell them.

A nice local fellow by the name of Gunther wrote a system for us that allows us to track our inventory, which is provided in this repository. Each item in our inventory has a sell-by date and a quality value. As each day passes, and the sell-by date gets closer, the quality of our watches degrades. Here are some specifics:

### Existing Requirements

- All items have a `SellIn` value which denotes the number of days we have to sell the items.
- All items have a `Quality` value which denotes how valuable the item is.
- At the end of each day, our system lowers both values for every item.

Additional rules:
- Once the sell-by date has passed, `Quality` degrades twice as fast.
- The `Quality` of an item is never negative.
- "Vintage Rolex" actually increases in `Quality` the older it gets.
- The `Quality` of an item is never more than 50.
- "Legendary Watch Face", being a legendary item, never has to be sold or decreases in `Quality`.
- "Passes to Watchface Conference", like the Vintage Rolex, increases in `Quality` as its `SellIn` value approaches:
    - `Quality` increases by 2 when there are 10 days or less.
    - `Quality` increases by 3 when there are 5 days or less.
    - `Quality` drops to 0 after the conference.
    - `SellIn` refers to the number of days until the conference.

Gunther claims he already implemented the above, but he is no longer available to work on this project, and we have recently signed a supplier of fragile items that requires an update to our system.

### New Requirement

- "Fragile" items degrade in `Quality` twice as fast as normal items.

We need you to take over his codebase and confirm it implements all existing and new requirements.

### Additional Notes

- Feel free to make any changes to the `UpdateQuality` method and add any new code as long as everything still works correctly. **However, do not alter the `Item` class or `Items` property as those belong to the goblin in the corner who will insta-rage as he doesn't believe in shared code ownership (you can make the `UpdateQuality` method and `Items` property static if you like, we'll cover for you).**
- Just for clarification, an item can never have its `Quality` increase above 50, however, "Legendary Watch Face" is a legendary item and as such its `Quality` is 80, and it never alters.

## Expected Deliverables

- The code must be runnable (as described in the language-specific README), and adhere to all the requirements listed above.
- The new ‘fragile’ item requirement must be implemented.
- The `Item` class and `Items` property have **not** been changed.
- It would be great if you improve on Gunther’s way of writing code, we’ve been told it’s not of the highest quality.
- As mentioned in the introduction, a fork of this repository with all the changes would be great. If you feel like a different way of delivering this code is better, feel free to do so!

Good luck!
