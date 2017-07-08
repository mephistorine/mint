# Mint - stylus framework

![](https://img.shields.io/badge/license-MIT-brightgreen.svg)

Use:
```stylus
@import 'mint/mint'

.container
  container 100%
  flex-row()

.col
  col 2
  col 2 'lg'
```
or
```stylus
@import 'mint/mint'

.container
  container( 100% )
  flex-row()

.col
  col( 2 )
  col( 2, 'lg' )
```

Yields:

```css
.container {
	max-width: 100%;
	padding-left: 30px;
	padding-right: 30px;
	margin: 0 auto;
	display: flex;
	flex-wrap: wrap;
}

.col {
	width: calc( 16.666666666666668% - 30px );
	padding-left: 15px;
	padding-right: 15px;
}

@media screen and (max-width: 1300px) {
	.container {
		padding-left: 30px;
		padding-right: 30px;
	}
}

@media screen and (max-width: 960px) {
	.container {
		padding-left: 20px;
		padding-right: 20px;
	}
}

@media screen and (max-width: 780px) {
	.container {
		padding-left: 2%;
		padding-right: 2%;
	}
}

@media screen and (max-width: 560px) {
	.container {
		padding-left: 1%;
		padding-right: 1%;
	}
}

@media screen and (max-width: 1300px) {
	.col {
		width: calc( 16.666666666666668% - 30px );
		padding-left: 15px;
		padding-right: 15px;
	}
}
```