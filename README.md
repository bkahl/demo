Steps for Standardizing Vision
====

## Asset Pipline Structure

```UI/assets
UI
   ├── javascripts
   │   └── app
   ├── sass
   │   ├── partials
   │   │    ├── components
   │   │    │   ├── _buttons.scss
   │   │    │   ├── _navbar.scss
   │   │    │   └── _dropdown.scss
   │   │    ├── sections
   │   │    │   ├── _accounts.scss
   │   │    │   └── _users.scss
   │   │    ├── _globals.scss
   │   │    └── _mixins.scss
   │   └── _variables.scss
   ├── themes
   │   └── vision
   │        ├── fonts
   │        ├── images
   │        ├── partials
   │        ├── _base.scss
   │        ├── _colors.scss
   │        ├── _pallette.scss
   │        ├── _images.scss
   │        ├── _fonts.scss
   │        ├── _variables.scss #overwrite default variables listed above
   │        ├── vision.scss
   │        └── config.rb
   ├── stylesheets
   │   └── vision.css #generated master.css file from selected theme
   └── index.html  #styleguide reference based off of the generated default.css 
```
   
## Sprites
### Structure
```Sprites
images
   └─ default #selected theme
      ├── logo-icon.png
      ├── top-bar-help.png
      ├── sub-bar-data.png
      ├── sub-bar-visulizations.png
      ├── sub-bar-sharing.png
      └── sub-bar-about.png
```

### How to Use
```html
/*_images.scss*/
@import "default/*.png";
```

```html
/*_navbar.scss*/
.navbar {
	&.logo {
		&:before {
			@include default-sprite(logo-icon);	
		}
	}
	&.help {
		&:before {
			@include default-sprite(top-bar-help);	
		}
	}
	&.data {
		&:before {
			@include default-sprite(sub-bar-data);	
		}
	}
	
	&.viz {
		&:before {
			@include default-sprite(sub-bar-visulizations);	
		}
	}

	&.sharing {
		&:before {
			@include default-sprite(sub-bar-sharing);	
		}
	}

	&.about {
		&:before {
			@include default-sprite(sub-bar-about);	
		}
	}
}
```

## Foundation 4 Pros and Cons
### Pros
1. Top/Sub Bar current DOM structure follows namespace and wouldn't need to be changed.
2. Namespace is simpliar.

### Cons
1. Less active community
3. Uses EM's vs Pixels.
4. Was more complex to leverage/manipulate for design purposes due to them styling/hard coding styles into namespace selectors which are less common (:after, :before).

## Bootstrap 3 Pros and Cons
### Pros
1. Easy to leverage/manipulate with ease.
2. Default global variables more intuitive.
3. More active community.

### Cons
1. Namespace more complex.
2. Top/Sub Bar current DOM structure would need to be changed to match Bootstrap's.

### Summary
I think it's too early to decide which to go with due to not prototyping Foundation 4 and Bootstrap 3's Block and Fluid grid layout, which is why these frameworks are used in the first place.
Currently, I think we could leverage either or, but it all depends on our redesign descision.  Ultimately we should leverage the framework 
that works easiest/best with our design goal.
