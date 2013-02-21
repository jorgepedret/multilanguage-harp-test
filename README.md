# Multilanguage test using Harp

__Quick project put together to test for ways to create multilanguage sites using [Harp](https://github.com/sintaxi/harp)__

## File Structure

```
/harp.json
/public
  /en
    _data.json
    ...
  /es
    _data.json
    ...
  /_layout.jade
```

### `/harp.json`

Used to specify a default language. In this case 'en'.

```
{
  "globals": {
    "default_lang": "en"
  }
}
```

### `/public/{ lang }/_data.json`

Translation for the navigation menu goes in these files. This could be done in other ways, but the purpose of it was to separate structure from content.

### `/public/_layout.jade`

We used some inline javascript to detect the selected language.


## Alternatives

For this particular case we made `/` ask you to choose a language, `/en` to go to english and `/es` to go to spanish. But you could figure out a way to show `/en` by default when you go to `/`.

You could also remove the need to add translations to `/{lang}/_data.json` by moving the the navigation markup to each language directory. Which would work really nice for smaller sites.







