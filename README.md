I have an idea, will implement later

````php
/**
 * @file /sites/default/settings.php
 */
$conf['at_seo_links_checking'] = function() {
  $config['pages'] = array(
    'entity' => array(
      'user' => array('user'),
      'node' => array('article'),
      'taxonomy_term' => array('tags', 'product_types'),
    ),
    'menu' => array('primary-links', 'footer-links'),
    'ctool_pages' => array(
      'about-us',
      'contact-us/%/%' => array(
        array('sales', 'director')
      )
    ),
    'custom_pages' => array(
      'ads', '/banner/new-year-events.png',
    )
  );

  $config['notification'] = array(
    'recipients' => array('webmaster@coolweb.com'),
    'check' => array('a', 'img', 'css', 'js', 'iframe', 'object', 'embed'),
  );

  return $config;
};
````

````bash
drush at-seo-links-checker
drush at-seo-links-checker --entity=node:*
drush at-seo-links-checker --entity=node:article
````
