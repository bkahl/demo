Steps for Standardizing Vision
====

## Asset Pipline Structure

```UI/assets
UI/assets
   ├── fonts
   ├── javascripts
   │   ├── vendor
   │   │   └── bootstrap/foundation
   │   └── app
   ├── sass
   │   ├── images
   │   │   └── default
   │   ├── vendor
   │   │   ├── bourbon
   │   │   ├── sassy-buttons
   │   │   └── bootstrap/foundation
   │   ├── partials
   │   │    ├── components
   │   │    │   ├── _buttons.scss
   │   │    │   ├── _navbar.scss
   │   │    │   └── _dropdown.scss
   │   │    ├── sections
   │   │    │   ├── _accounts.scss
   │   │    │   └── _users.scss
   │   │    ├── _base.scss
   │   │    ├── _images.scss
   │   │    ├── _fonts.scss
   │   │    ├── _globals.scss
   │   │    └── _mixins.scss
   │   ├── _variables.scss
   │   └── default.scss
   ├── stylesheets
   │   └── default.css #generated master.css file
   ├── config.rb
   └── index.html  #styleguide reference based off of the generated default.css 
```

## Sprites
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

## Foundation Pros and Cons
###Pros
1. Top/Sub Bar current DOM structure follows namespace.
2. Namespace is simpliar

### Cons
1. Less active community
2. No IE 8 support for fluid grid, basic components work though
3. Uses EM's vs Pixels
4. Was more complex to leverage/manipulate for design purposes due to them styling/hard coding styles into namespace selectors which are less common (:after, :before).

