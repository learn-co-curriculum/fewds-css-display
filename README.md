## Objectives:

1. Different ways that elements display by default
2. How that will affect the size and space the elements 

### Display Settings
By default, certain elements display `inline`, whereas other elements may display `block`. Elements that display inline will appear side-by-side, and do not accept a width, or a top and bottom margin. Elements that display block will always display one on top of the other, meaning vertically. Their width will automatically take up the whole line if the width is not specified, and they'll be able to have a top and a bottom margin.

### Setting Display Properties
You can set elements to display `inline-block`, and also `table` and `table-cell`, among others, but you'll focus on the first two to start off with. 

<iframe width="100%" height="300" src="//jsfiddle.net/flatiron_school/352A6/1/embedded/html,css,result/" allowpaymentrequest allowfullscreen="allowfullscreen" frameborder="0"></iframe>

In this simple example, there are two divs with two spans inside of them labeled A, B, C and D. The divs are set to have a blue background color and the spans have a pink background color. The divs by default automatically display block in the browser. Certain elements are
always display block, unless you specify otherwise. such as paragraphs and headings--among others. In the example, A is stacked above B because it's displaying as a block, and a width hasn't been specified. 

### Block & Inline Elements
Block level elements are like greedy kings of the horizontal
space, and the inline elements are like friendly hippies that will hang out next to each other, side-by-side. Block level elements will expand to 100% of the width unless change the properties for display. 

Spans are *also* containers, but they display inline by default. In the example, inline elements display on the same line. Spans are only going to be as wide as the content that's inside of them, as well as other inline elements. Other inline elements include the `<a>` tag for links and images using the `<img>` tag. If you specify a width to an element such as a span that displays inline, it will ignore the width. For example, if the spans are set to 200px width, you won't see it because it's being ignored, and the width of the element will not change. When 10px of margin is set on these inline elements, you'll notice that there is 10px marging on the sides, but not above and below. 

[block example]

Block level elements can have margin on all sides and they can have a width specified. On block level elements, the margin on the top and bottom of elements are collapsed. On the div, there's a margin of 10px on each side. Div A has 10px on the bottom, and Div B
block has a margin of 10px on the top. Instead of this combining into 20px of margin in between--they overlap each other. You will only see 10px of margin in and not 20px. The margins on the left and right of the spans are not overlapping. The left and right margin actually combine, and you can see a 20px gap. 

### The Display Property
In CSS there there is a `display` property which will allow us to set the way elements are displayed, and override their defaults. You can make a div behave like a span, or make a span behave like a div, simply by setting its `display`. 

[span set to block]

If you set the span to `display: block`, you'll notice that they begin to appear with a width, with margin above and
below while stacking vertically.

In addition to `block` and `inline` you also have the
ability to set elements to to `display: inline-block`. Inline-block gets some of the characteristics of inline and block. When both sets of containers are set to inline-block, they exist side-by-side with each other, are able to have margin on the top and bottom, and have a width specified. 

[table-cell example]

We can also set elements to `display: table` and `display: table-cell`. In this example, you can see that table cell does not have the ability to have a margin on the sides. Instead, it's trying to make these elements act like they are the cells of a table. 

[table-cell collapse]

If you remove the width setting on the table cells, you'll notice that they will collapse to the size of the content. 

[inline block example]

When creating a page layout, you might want to specify a width and be able to have margin or spacing between the elements. You might think that inline-block would be the way to go, but it turns out there's some funny things that will happen. You can see that the amount of padding inside of these elements between the divs and the spans are different and are not aligning with either the bottom or the top of this other columns properly. For this reason you have a different strategy all together for creating column structure in a traditional layout by setting elements to display block but then using another property such as floating to get them to position side by side.
