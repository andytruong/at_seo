I have an idea, will implement later


````yaml
at_seo_links_checking:
  entity:
    user: [user]
    node: [article]
    taxonomy_term: [tags, product_types]
    menu: [primary-links, footer-links]
  ctool_pages:
    'about-us'
    contact-us/%/%: ['sales', 'director']
    custom_pages: [ads, '/banner/new-year-events.png']
  notification:
    recipients: ['webmaster@coolweb.com']
    check: [a, img, css, js, iframe, object, embed]
````

````bash
drush at-seo-links-checker
drush at-seo-links-checker --entity=node:*
drush at-seo-links-checker --entity=node:article
````
