# dspace7.6 A Dropdown for the menu in the dspace theme

This code allows you to add a drop down to the menu bar in dspace 7.6

In the folder dspace-angular-dspace-7.6/src/themes/dspace/app/navbar

place the folder <b>drop-about</b>

This folder is just a component. It contains an scss file, an html file and a ts file.


To use this component you need to modify three files:
1) dspace-angular-dspace-7.6/src/themes/dspace/eager-theme.module.ts
2) dspace-angular-dspace-7.6/src/themes/dspace/app/navbar/navbar.component.ts
3) dspace-angular-dspace-7.6/src/themes/dspace/app/navbar/navbar.component.html

<b><u>Directions</u></b>

1) In order for this component to be available it needs to be added to eager-theme.module.ts in two places.

A) at the top add an import statement:<br>
import { DdAboutComponent } from './app/navbar/drop-about/dd-about.component';

B) in the  const DECLARATIONS add it:<br>
  DdAboutComponent,


2) In navbar.component.ts add an import statment:<br>
    import {DdAboutComponent } from './drop-about/dd-about.component';

3) In navbar.component.html add it to the navbar in the section   ```<div id="collapsingNav" class="w-100 h-100">```

    ```<ds-dd-about class="navbar-collapsed nav-item d-flex align-items-center"></ds-dd-about>```
    
    
You can now compile and see the dropdown. It is easy to change by modifying the html or css

https://wiki.lyrasis.org/display/DSDOC7x/User+Interface+Customization#UserInterfaceCustomization-CustomizeNavigationLinksinHeader
