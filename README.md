## i18n Jquery, Backbone, Underscore Example
Integration of i18next intl lib 

## Overview
 - [x] jquery, backbone, underscore, i18next, jqueryi18n
 - [x] i18n -> en-US, de-DE
 - [x] common -> global labels like buttons, input boxes, title etc.
 - [x] validation -> error message globally across the app
 
 ## Key Aspects while configuring i18next
 
 ```
 .use(i18nextHttpBackend) : Ajax way to load i18n
  load: 'currentOnly' : if you want to disable "en" by default
  fallbackNS: false
 ```
 
 ## General problem
 Most of time, we have problem's with 'common' properties loading. For few clients, we have to update only ```specific keys``` but still want to keep rest of key's from the common.
 
 recommended solution:
 ```
 Important: you can load the specific client namespace i18n file and merge it with 'common' which helps in this situations.
 it will override the specific keys and keep rest of them intact.
 ```
 ```
 i18next.loadNamespaces([client],function(){
          i18next.addResourceBundle(lng, 'common',
          i18next.getResourceBundle(lng,client),true,true);
        });
 ```
 
 ### how to use
 <a  href="#" data-i18n="[title]button.continue;[html]button.continue">Testing</a>
 we can use mulitple notation: helps in SEO for image tags or a href.
 
 Hope this solution help in your coding !! Happy Coding !! 
 
 Feel free to use
