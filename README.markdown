## Nested responsive grids
Generate a responsive grid that maintains it&rsquo;s column sizes two levels deep. <a href="http://davist11.github.com/nested-responsive-grid/">View Demos</a>.

### Bootstrap&rsquo;s Nested Responsive Grid
When using another grid framework (like Twitter Bootstrap), nested grids get weird:

>Nesting with fluid grids is a bit different: the number of nested columns doesn't need to match the parent. Instead, your columns are reset at each level because each row takes up 100% of the parent column.

<pre>&lt;div class="row-fluid">
	&lt;div class="span6">
		6
		&lt;div class="row-fluid">
			&lt;div class="span6">3&lt;/div>
			&lt;div class="span6">3&lt;/div>
		&lt;/div>
	&lt;/div>
&lt;/div></pre>

That means that the sub columns will each be a &ldquo;3&rdquo; column. But, that 3 column width will not be the same as a standalone 3 column since it is a percentage of another percentage. It&rsquo;s kind of hard to explain, but the below image should illustrate the problem.

![Bootstrap Nested Responsive Grid Demo](https://github.com/davist11/nested-responsive-grid/raw/master/images/nested-bootstrap.png)

### My Nested Responsive Grid
I hated that. So in my system, a &ldquo;3&rdquo; sub-column would equal the width of a standalone 3 column

<pre>&lt;div class="row">
	&lt;div class="span6">
		6
		&lt;div class="row">
			&lt;div class="span3">3&lt;/div>
			&lt;div class="span3">3&lt;/div>
		&lt;/div>
	&lt;/div>
&lt;/div></pre>

![Nested Responsive Grid Demo](https://github.com/davist11/nested-responsive-grid/raw/master/images/nested.png)