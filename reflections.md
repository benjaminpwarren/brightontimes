# Lesson 5 / Home Town App / Brighton Times
## Hero

### Responsive Background Image

I calculated the image aspect ratio and then put a height in `vw` units on the hero to make the height relative to the width. This operates the `550px` breakpoint at which point it switches back to the original `300px` height, which of course crops the image horizontally.

In this image the subjects are always visible but with different images, `background-position` and possibly alternative images might have to be used to accommodate different screen sizes/ratios.

http://stackoverflow.com/questions/20590239/maintain-aspect-ratio-of-div-but-fill-screen-width-and-height-in-css

### Description

I hid the sub-description until the `389px` breakpoint and removed the `height:40%` of description.

I also made `h2` font-size be relative to the viewport width until the `389px` breakpoint.

https://css-tricks.com/viewport-sized-typography/

## Top-News

Removed `max-height: 300px` and set `padding-bottom: 0` as the last item was partially hidden under the Scores table where narrow viewport.

## Scores

I was originally playing with rearranging table columns by switching the `tr`s to `display:flex` and the `td`s then behaving like flex-items, but I was concerned about the potential impact on accessibility doing it that way (actually testing the impact could potentially have burned up a lot of time).

http://stackoverflow.com/questions/7373177/can-html-table-cells-be-rearranged-with-css

Another option would be to use CSS `content` to merge some of the columns. (Though it would be easier to just edit the HTML!)

https://developer.mozilla.org/en/docs/Web/CSS/content

In the end, I just decided to hide the *Date* and *Location* columns and display them at `290px` and `390px` respectively.

I still think the table still looks ugly between `550px` and `700px` but I couldn't think of an easy solution. One option would be getting the logos for the teams and displaying them too.

## Latest News

### Snippet

Snippets take up 100% of width until the `850px` breakpoint at which point they change to 50%.

### Snippet Thumbnails

I changed the `snippet__thumbnail` images with be `width:25%` with `min-width:80px`. This makes them a decent size but doesn't let them shrink so small as to make their subjects indistinguishable.

## Footer

I changed the footer so the items are `width:33.333333%` above 270px, and `width:100%` below that.

Additionally, I centered them vertically and horizontally. The vertical centering means the *Follow us on Twitter* text still looks good when it's wrapped due to the viewport width.

https://philipwalton.github.io/solved-by-flexbox/demos/vertical-centering/

http://stackoverflow.com/questions/2717480/css-selector-for-first-element-with-class