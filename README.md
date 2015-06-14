# flatnuke-cookie-law
Make Flatnuke to be compliant with EU Cookie Law.
  
This plugin is based on the open source project **Cookie Consent** https://silktide.com/tools/cookie-consent/

## Installation
1. upload the content of the directory `include` to the root of your site
2. upload the content of the directory `sections` to the root of your site

## Create a new link in site's footer
All the pages of your site MUST have a link to the page in which you describe your cookie policy, so
you have to modify your Flatnuke theme.
  
Edit the file `/themes/<your theme>/theme.php`, look at the function CreateFooterSite() and substitute:
```
echo $footer_elements['legal']."<br />";
```
with this:
```
echo $footer_elements['legal']." | <a href='index.php?mod=none_Cookie_Policy'>Cookie Policy</a><br />";
```

## Configuration
You can customize the layout of the alert by the file `/include/javascripts/cookie_policy.js`
  
https://silktide.com/tools/cookie-consent/docs/

## Info

### Author
Marco Segato

### Version
20150614

###License
GNU GENERAL PUBLIC LICENSE Version 2