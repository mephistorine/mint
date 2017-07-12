<style>
  pre{
    tab-size: 2;
  }

  .mint-logo{
    transform: rotate(45deg);
    width: 100px;
  }
</style>
<img src='assets/Mint.svg' class='mint-logo'>

![](https://img.shields.io/badge/license-MIT-brightgreen.svg)
![](https://img.shields.io/badge/release-v0.0.2-green.svg?colorB=7effd4)
# Mint - stylus framework

Mint is a simple stylus framework

Use:
```stylus
@import 'mint/mint'

.container
  container(100%)
  flex-row()

.col
  col(2) // for all devices
  col(2, 'lg') // only large
```

> Mint generates a lot of media queries that would sort them using the [gulp-combine-mq](https://www.npmjs.com/package/gulp-combine-mq) plugin

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
Yelds with gulp-combine-mq:
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

  .col {
		width: calc( 16.666666666666668% - 30px );
		padding-left: 15px;
		padding-right: 15px;
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
```

## License
	MIT (c) Mint CSS