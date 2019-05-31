# angulat-strict-css
Based on https://github.com/angular/angular/issues/6361#issuecomment-438870935 suggestion

#### How does it work?
* Remove styleUrls from `@Component`
* Use good old css (<- it should work with a preprocessor)
* Remove inline styles from the html files
* add a meta tag with a strict csp policy

```
  <meta http-equiv="Content-Security-Policy" content="default-src 'self'; img-src 'self' data:">
```

Enjoy!

```
ng build --aot --prod
```
