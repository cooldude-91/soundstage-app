# SoundStage web pages

Support and privacy pages for the SoundStage iPhone app, published with GitHub Pages, and the launch-offer file the app
reads.

## offers.json: the Lifetime launch price

While the date in `ends` is in the future, the app shows under Lifetime: "Launch price: save 40%" and how many days are
left. After that date it shows nothing. The price itself always comes from the App Store, so set both together:

1. In App Store Connect, set Lifetime's launch price (for example $29.99) now, and schedule the regular price (for
   example $49.99) to start on the end date.
2. Here, set `ends` to that same moment (UTC, like `2026-11-12T00:00:00Z`) and `saving` to the whole percent saved
   (29.99 against 49.99 is 40). Edit the file on GitHub (the pencil icon) and commit.

The app checks the file when it opens and when it comes back on screen (at most once an hour). The request carries
nothing about the person.
