# dspace7.6Dropdpown
The code for adding a drop down to the navbar
https://wiki.lyrasis.org/display/DSDOC7x/User+Interface+Customization#UserInterfaceCustomization-CustomizeNavigationLinksinHeader

This code allows you to add a drop down to the navigation bar in dspace 7.6

In the folder dspace-angular-dspace-7.6/src/themes/dspace/app/navbar

place the folder drop-about

This folder is just a component. It contains an scss file, an html file and a ts file.


To use this component you need to modify three files:
1) dspace-angular-dspace-7.6/src/themes/dspace/eager-theme.module.ts
2) dspace-angular-dspace-7.6/src/themes/dspace/app/navbar/navbar.component.ts
3) dspace-angular-dspace-7.6/src/themes/dspace/app/navbar/navbar.component.html

1) In order for this component to be available it needs to be added to eager-theme.module.ts in two places.

A) at the top
import { DdAboutComponent } from './app/navbar/drop-about/dd-about.component';

B) in const DECLARATIONS = [
  DdAboutComponent,




2) In navbar.component.ts add this line:

    import {DdAboutComponent } from './drop-about/dd-about.component';

3) In navbar.component.html add this to your <div id="collapsingNav" class="w-100 h-100">

    <ds-dd-about class="navbar-collapsed nav-item d-flex align-items-center"></ds-dd-about>
    
    
You can now compile and see the dropdown. It is easy to change by modifying the html or css
