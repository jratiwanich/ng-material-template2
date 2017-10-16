# Ng Material Template1
This is the seed template for Material custom theme and color palette using [Angular Material](https://material.angular.io/) and (Materializecss)[http://materializecss.com]. The time of writing this, Angular Material does not support all of the Materializecss yet.

| Component	  | Materialize	| Angular material 2 |
|-------------|-------------|--------------------|
| buttons	    | Yes	        | Yes	               |
| Badges	    | Yes	        | No	               |
| Breadcrumbs	| Yes	        | No	               |
| Cards	      | Yes	        | Yes	               |
| Chips	      | Yes	        | No		             |
| Collections |	Yes	        | Yes	               |
| Footer	    | Yes	        | No	               |
| Icons	      | Yes	        | Yes	               |
| Navbar	    | Yes	        | No	               |
| Pagination	| Yes	        | No	               |
| Preloader	  | Yes	        | Yes	               |
| SideNav	    | Yes	        | Yes	               |
| Carousel	  | Yes	        | No	               |
| Table	      | Yes	        | No	               |
| Collapsible	| Yes	        | No	               |
| Dialogs	    | Yes	        | Yes	               |
| Parallax	  | Yes	        | No                 |


| Forms	          | Materialize	| Angular material 2 |
|-----------------|-------------|--------------------|
| Input           | Yes         | Yes                |
| Select          | Yes         | Yes                |
| Radio           | Yes         | Yes                |
| Checkbox        | Yes         | Yes                |
| Switches        | Yes         | Yes (Slide toggle) |
| File Input      | Yes         | No                 |
| Range           | Yes         | Partial            |
| Date Picker     | Yes         | Yes                |
| Time Picker     | Yes         | No                 |
| Character Count | Yes         | No                 |
| Autocomplete    | Yes         | Yes                |


### * Material CSS classes will not be supported in Angular Material.
___

1) Install

  * these for Angular Material:
```
@angular/material
@angular/cdk
@angular/animations
hammerjs
```
  * install for Materialcss
```
materialize-css
angular2-materialize
```

2) Add Meterial icons

`<link href="https://fonts.googleapis.com/icon?family=Material+Icons" rel="stylesheet">`

3) Add Material prebuild theme with one of the followings:
Import in `styles.css` or add the link in the `index.html`

* deeppurple-amber.css
* indigo-pink.css
* pink-bluegrey.css
* purple-green.css

styles.css use - `@import '~@angular/material/prebuilt-themes/deeppurple-amber.css';`
index.html use - `<link href="https://unpkg.com/@angular/material/prebuilt-themes/indigo-pink.css" rel="stylesheet">`

4) Import Material API into app.module.ts

```
import {MatChipsModule,MatButtonModule} from '@angular/material';
...
imports: [
  BrowserModule,
  MatChipsModule,
  BrowserAnimationsModule,
  MatButtonModule
]
```

___

## (OPTIONAL) Custom Theme follow these steps:

1) Modify angular-cli.json and change from css to scss
```
"styles": [
  "styles.scss"
]
...
"defaults": {
  "styleExt": "scss",
  "component": {}
}

```

2) Remove the default Meterial css theme from styles.css or index.html

3) Add the following lines in styles.scss

```
@import '~@angular/material/theming';
@import 'myfirst-theme.scss';
@include mat-core();

@include angular-material-theme($myfirst-theme);
```
where you will create a custom theme in `myfirst-theme.scss` and add in the global theme in Angular Material

4) Create a new file `myfirst-theme.scss` and change primary, accent, and warning colors. You can use the standard color palette name from [Material color guidelines](https://material.io/guidelines/style/color.html#color-color-palette)

5)
