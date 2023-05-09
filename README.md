# Enhanced-Ecommerce
Implementation Documents of Enhanced Ecommerce in GA4 - Hamrahmechanic

Google Analytics 4 Enhanced Ecommerce: Data Layer specification for www.hamrah-mechanic.com

Why is this needed? Enhanced Ecommerce feature in Google Analytics enables businesses to track the entire ecommerce funnel (starting from product impressions and ending with a purchase. Enhanced Ecommerce will let us identify the weak spots of the visitor’s journey (where they are dropping off) and improve them, therefore, increase revenue.

Goal: On certains pages or on certain interactions implement dataLayer.push snippets that contain the Ecommerce data. This information will be then captured by Google Tag Manager and automatically sent to Google Analytics 4.

Useful resources for reference: 
https://developers.google.com/tag-manager/enhanced-ecommerce
https://developers.google.com/analytics/devguides/collection/analyticsjs/enhanced-ecommerce
https://www.simoahava.com/analytics/enhanced-ecommerce-guide-for-google-tag-manager/ 

Support for questions: behzad.bolourchi@gmail.com

Pages of implementation: 
There will be multiple pages and interactions where different dataLayer.push snippets must be implemented. at first we just start with simplest funels and landings that we have in Hamrahmechanic website.
* Purchase in sell funel
when a successful purchase was made (no matter payed or not, user just land on thank you page)

Code location: Does not matter, just make sure that every code is activated only when the situation/interaction meets the description that I’ve provided below and loaded before tagmanager script.


Things to keep in mind:
* For different situations/interactions different tracking codes must be implemented
* dataLayer.push code snippets must follow the strict data structure that I have provided in the codes. If you think that some other custom parameters should be included (or something is missing), please let me know and we will discuss this.
* Money-related data must be formatted in a following way:
 * type: string
 * contains: only a number separated by a decimal point, 
 * separator: dot
 * Good example: ‘14.00’
 * Bad examples: ‘15,00’, ‘20.00 EUR’, ‘$5.00’
