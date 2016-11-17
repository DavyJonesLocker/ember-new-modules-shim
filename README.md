# Ember New Modules Shim

This is a shim addon that declares ES6 modules that shim the Ember global,
according to the new [JavaScript Modules API RFC](https://github.com/emberjs/rfcs/pull/176).

## Warning

This is an expirimental shim. This is for science, not for profit.

Keep in mind that as this RFC evolves so will the addon so if you're adverse to churn in your app you may not want to opt in yet.

## Installation

```
ember install ember-new-modules-shim
```

## (Optional) Disabling `ember-cli-shims`

I recommend doing this after making the transition.

Start with uninstalling the `ember-cli-shims` Bower module:

```
bower uninstall ember-cli-shims --save
```

Then add the following config to your `EmberApp` in your `ember-cli-build.js` file:

```
module.exports = function(defaults) {
  var app = new EmberApp(defaults, {
    vendorFiles: {
      'app-shims.js': null
    }
  });

  return app.toTree();
};
```

## Legal

[DockYard](http://dockyard.com/ember-consulting), Inc. &copy; 2016

[@dockyard](http://twitter.com/dockyard)

[Licensed under the MIT license](http://www.opensource.org/licenses/mit-license.php)
