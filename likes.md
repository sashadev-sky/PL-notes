## PL website currently

![](./Giphy01.gif)

- varied results and can go into positive and negative double digits
- notification popups lag a substantial amount

- on page refresh, the likes count normalizes; resets to orginal count (+ or - 1 like). A single notification popup reflecting the last 'like' action also appears.

## Localhost before code updates

![](./Giphy02.gif)

- testing on another note for consistency

- the results are completely different from the live site and on the unstable branch 
  - the count always behaves normally
  - cannot reproduce the main prior issue in the development environment

- the notification popups continue to lag

## Unstable branch after code updates

![](./Giphy03.gif)

- liking and unliking is consistent on unstable as well now - the count is behaving normally

- notification popups are still lagging and misleading - (see the console output logging the notification's text right before a call to render it is made)


