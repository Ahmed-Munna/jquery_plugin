# Parallaxie
Parallaxie is a jQuery plugin to create parallax effects on your websites or templates. It is very lightweight to download and rendering by your browser.

### Current Version:
0.5

### Dependency:
This plugin has only one dependency, which is `jQuery`

### Demo:

Watch Parallaxie in action: http://static.theultrasoft.com/parallaxie/demo/

### License:
Licensed under the MIT License (LICENSE.txt)

Copyright (c) 2016 THE ULTRASOFT (http://theultrasoft.com)

### Installation:
Installing this plugin is very easy.
You have to include jQuery and Parallaxie scripts to your website.
```
<script src="js/jquery.min.js"></script>
<script src="js/parallaxie.min.js"></script>
```

Fire up the plugin with any css selector. You must have a background image set into that element or you can use the `data-image` attribute, will explain about this later. Also, make sure the parallax element must have some height or some content which has some height.

```
<style>
.parallaxie{
    min-height: 360px;
}
</style>
<div class="parallaxie" style='background: url("path/to/your/image.png")'></div>
<script>
$('.parallaxie').parallaxie();
</script>
```

View a more intutive [Parallaxie example](http://theultrasoft.com/project/parallaxie).

### Options:

You can easily customized this plugin any time.

#### 1. On initialization:
This method gives you a quick configuration option.

```
<script>
$('.parallaxie').parallaxie({
	speed: 0.5,
	offset: 50,
	...
	...
});
</script>
```

#### 2. On declaration:
On declaration of the parallaxie element you can specify the option using the `data-parallaxie` attribute. This gives you to control or customize different parallaxie elements with different configurations.

```
<div class="parallaxie" style='background: url("path/to/your/image.png")' data-parallaxie='{
	"speed": -0.4
	"size": "auto"
}'></div>
```

| Option | Description | Default |
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------|-------------|
| speed | Speed of the parallax. You can use any floating point number. But practically, give any fractional number between -1 and 1. Example: 0.3 or -0.5 | 0.2 |
| repeat | Should the background repeat or not. Possible values: 'repeat', 'repeat-x', 'repeat-y', 'no-repeat' | 'no-repeat' |
| size | background size of the image. Possible values: 'auto', 'contain', 'cover' | 'cover' |
| pos_x | Position of the image horizontally. Possible values: 'left', 'center', 'right' or any percentage like: '30%' | 'center' |
| offset | The parallax offset. Possible values: Any integer. | 0 |