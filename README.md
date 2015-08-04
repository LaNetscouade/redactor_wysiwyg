redactor
========

Drupal 7 redactor wysiwyg adapter

## Add a redactor plugin

You have to implement `hook_redactor_plugins`

```
/**
 * Implements hook_redactor_plugins().
 */
function my_module_redactor_plugins($editor) {

  return array(
    'my_plugin_id' => array(
      'name' => 'My plugin',
      'files' => array(
        'js' => array(
          $editor['library path'] . '/plugin.js',
        ),
        'css' => array(
          $editor['library path'] . '/plugin.css',
        ),
      ),
      'config' => array(
          'param1' => 'value1',
          'param2' => 'value2'
      ),
    ),
  );
}
```

