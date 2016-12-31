# Liquid Grid
Flexible and Simple Grid System.

Liquid Grid adjust itself accordandly to the container dimensions.

![Liquid Grid](https://media.giphy.com/media/O0AEyXviC1vtC/giphy.gif)

- Easy.
- Semantic & Expressive.
- Inspired in [Jeet.gs](http://jeet.gs)

## Usage

A grid with 3 collumns and 20px gutters:

In sass:
```sass
ul {
	@include grid( 3, 20px );
	li {
		background-color: #ededed;
		margin-bottom: 15px;
		padding: 0 15px;
	}
}

```
In stylus:
```sass
ul
	grid( 3, 20px );
	li
		background-color: #ededed;
		margin-bottom: 15px;
		padding: 0 15px;
	


```

Output ( container with 800px )

![grid 800px](images/800px.png)

A collumn with different size:

In Sass:
```sass
ul {
	@include grid( 3, 20px );
	li {
		background-color: #ededed;
		margin-bottom: 15px;
		padding: 0 15px;
		&.double {
			@include col( 2/3 );
		}
	}
}

```

In Stylus:
```sass
ul
	grid( 3, 20px );
	li
		background-color: #ededed;
		margin-bottom: 15px;
		padding: 0 15px;
		&.double
			col( 2/3 );

```


Output ( container with 600px )

![grid 600px](images/double-size.png)


# API

### Sass: @include grid( n collumns, gutter width(px) )
### Stylus: grid( n collumns, gutter width(px) )

### Sass: @include col( collumns / n collumns, [ gutter width(px) ] )
### Stylus: col( collumns / n collumns, [ gutter width(px) ] )

If gutter is not passed in .col(), it will inherit from .grid() gutter's value ( default = 0 ).

#### Version 0.1.1

- Should work on IE9+
