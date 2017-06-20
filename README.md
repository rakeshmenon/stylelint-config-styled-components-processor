# `stylelint-config-styled-components-processor`

> The shareable stylelint config for [stylelint-processor-styled-components](https://github.com/styled-components/stylelint-processor-styled-components)

When using `stylelint-processor-styled-components` a couple of stylelint rules throw errors that you
cannot prevent. Like '[no-empty-source](https://stylelint.io/user-guide/rules/no-empty-source)' or 
'[no-missing-end-of-source-newline](https://stylelint.io/user-guide/rules/no-missing-end-of-source-newline)'.

This shareable config will automatically disable rules that cause unresolvable conflicts. Besides
those rules vendor prefixed [properties](https://stylelint.io/user-guide/rules/property-no-vendor-prefix)
and [values](https://stylelint.io/user-guide/rules/value-no-vendor-prefix) will throw an error since
styled-components automatically generates vendor prefixes for your css.

Note that if you want to change any of these rules you can always override them in your stylelint
config.

## installation

```
npm install stylelint-config-styled-components-processor --save-dev
```

## usage

After installing, add this config to your stylelint config like so:

```
{
  "extends": "stylelint-config-styled-components-processor"
}
```

If you're extending multiple shareable configs, put this config as the first so it overrides all
following rules like so:

```
{
  "extends": [
    "stylelint-config-styled-components-processor"
    "stylelint-config-standard",
  ]
}
```

See also https://stylelint.io/user-guide/configuration for documentation on the various ways
stylelint can be configured.

## license

[MIT](http://ismay.mit-license.org/)
