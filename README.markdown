Nested responsive grids

Generate a responsive grid that maintains it's appropriate sizes one level deep.

When using another grid framework (like bootstrap), nested grids get weird:


>Nesting with fluid grids is a bit different: the number of nested columns doesn't need to match the parent. Instead, your columns are reset at each level because each row takes up 100% of the parent column.

<pre>&lt;div class="row-fluid">
	&lt;div class="span6">
		Level 1 of column
		&lt;div class="row-fluid">
			&lt;div class="span6">Level 2&lt;/div>
			&lt;div class="span6">Level 2&lt;/div>
		&lt;/div>
	&lt;/div>
&lt;/div></pre>

That means that the sub columns will each be a "3" column. But, that 3 column width will not be the same as a standalone 3 column.

I hated that. So in my system, you would do it like this. And that 3 sub column would equal the width of a standalone 3 column

<pre>&lt;div class="row">
	&lt;div class="span6">
		Level 1 of column
		&lt;div class="row">
			&lt;div class="span3">Level 2&lt;/div>
			&lt;div class="span3">Level 2&lt;/div>
		&lt;/div>
	&lt;/div>
&lt;/div></pre>