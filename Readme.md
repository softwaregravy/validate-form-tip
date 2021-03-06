# validate-form-tip

  A tooltip error message plugin for validate-form.

## Installation

    $ component install segmentio/validate-form-tip

## Example

![](https://i.cloudup.com/E8uGdvIfZM.png)

```js
var validate = require('validate-form');
var tip = require('validate-form-tip');
var form = document.querySelector('form');

validate(form)
  .use(tip({ position: 'west' })
  .field('username')
    .is('required')
    .is(function (val, done) {
      isUnique(val, function (err, res) {
        done(res.body.unique);
      });
    });
```

## API

### tip(options)
  
  Generate the `tip` plugin for `validate-form` with `options`:

    {
      duration: Number,
      effect: String,
      position: String
    }
  
## License

  MIT
