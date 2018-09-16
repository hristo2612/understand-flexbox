# understand-flexbox
Repository which will serve as a future reference to highlight what flexbox can actually do!

## Chapter 1

### The two axes of flexbox

When working with flexbox you need to think in terms of two axes — the main axis and the cross axis. The main axis is defined by the flex-direction property, and the cross axis runs perpendicular to it. Everything we do with flexbox refers back to these axes, so it is worth understanding how they work from the outset.

The main axis is defined by <b>flex-direction</b>, which has four possible values:

<b>row</b>

<b>row-reverse</b>

<b>column</b>

<b>column-reverse</b>

### The flex container

An area of a document laid out using flexbox is called a <b>flex container</b>. To create a flex container, we set the value of the area's container's <code>display</code> property to <code>flex</code> or <code>inline-flex</code>. As soon as we do this the direct children of that container become <b>flex items</b>. As with all properties in CSS, some initial values are defined, so when creating a flex container all of the contained flex items will behave in the following way.

<ul>
    <li>Items display in a <code>row</code> (the <code>flex-direction</code> property's default is <code>row</code>).</li>
    <li>The items start from the start edge of the main axis.</li>
    <li>The items do not stretch on the main dimension, but can shrink.</li>
    <li>The items will stretch to fill the size of the cross axis.</li>
    <li>The <code>flex-basis</code> property is set to <code>auto</code>.</li>
    <li>The <code>flex-wrap</code> property is set to <code>nowrap</code>.</li>
</ul>

The result of this is that your items will all line up in a <code>row</code>, using the size of the content as their size in the main axis. If there are more items than can fit in the container, they will <b>not</b> <code>wrap</code> but will instead <code>overflow</code>. If some items are taller than others, all items will stretch along the cross axis to fill its full size.

[Example 1](https://mdn.github.io/css-examples/flexbox/basics/the-flex-container.html)


#### Changing flex-direction

We can change the direction of our items by using <code>flex-direction</code>!

[Example 2 - with row-reverse](https://mdn.github.io/css-examples/flexbox/basics/flex-direction.html)


### Multi-line flex containers with <code>flex-wrap</code>

While flexbox is a one dimensional model, it is possible to cause our flex items to wrap onto multiple lines. In doing so, you should consider each line as a new flex container. Any space distribution will happen across that line, without reference to the lines either side.

To cause wrapping behaviour add the property <code>flex-wrap</code> with a value of wrap. Now, should your items be too large to all display in one line, they will wrap onto another line. The live sample below contains items that have been given a width, the total width of the items being too wide for the flex container. As <code>flex-wrap</code> is set to <code>wrap</code>, the items wrap. Set it to <code>nowrap</code>, which is also the initial value, and they will instead shrink to fit the container because they are using initial flexbox values that allows items to shrink. Using <code>nowrap</code> would cause an overflow if the items were not able to shrink, or could not shrink small enough to fit.

[Example 3 - flex-wrap](https://mdn.github.io/css-examples/flexbox/basics/flex-wrap.html)


[Resources from here](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Flexible_Box_Layout/Basic_Concepts_of_Flexbox)
