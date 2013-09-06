# Field Configure

Field Configure is a Drupal module that provides helpers to create fields and instances of fields from code. This makes it possible to define fields using Kraftwagen Manifests, instead of using Features.

# Usage

```php
$field = array(
  'field_name' => 'body',
  'type' => 'text_with_summary',
  'entity_types' => array('node'),
);
field_configure_field($field);

$instance = array(
  'field_name' => 'body',
  'entity_type' => 'node',
  'bundle' => 'page',
  'label' => 'Body',
  'widget' => array(
    'type' => 'text_textarea_with_summary',
    'weight' => 0,
  ),
  'settings' => array('display_summary' => TRUE),
  'display' => array(
    'default' => array(
      'label' => 'hidden',
      'type' => 'text_default',
    ),
    'teaser' => array(
      'label' => 'hidden',
      'type' => 'text_summary_or_trimmed',
    ),
  ),
);
field_configure_instance($instance);
```

