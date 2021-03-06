# cz-emoji

> Commitizen adapter formatting commit messages using emojis.


**cz-emoji** allows you to easily use emojis in your commits using [commitizen].

```sh
? Select the type of change you are committing: (Use arrow keys)
❯ feature   🌟  A new feature
  fix       🐞  A bug fix
  docs      📚  Documentation change
  refactor  🎨  A code refactoring change
  chore     🔩  A chore change
```

## Install

```bash
npm install --global cz-emoji

# set as default adapter for your projects
echo '{ "path": "cz-emoji" }' > ~/.czrc
```

## Usage

```sh
$ git cz
```

## Customize

You can customize things for a project by adding a configuration section in your `package.json`:

```json
{
  "config": {
    "cz-emoji": {}
  }
}
```

### Types

An [Inquirer.js] choices array:
```json
{
  "config": {
    "cz-emoji": {
      "types": [
        {
          "name": "feature \t🌟  A new feature",
          "value": ":star2:"
        }
      ]
    }
  }
}
```

The value `property` must be the emoji itself.

### Scopes

An [Inquirer.js] choices array:
```json
{
  "config": {
    "cz-emoji": {
      "scopes": [
        "home",
        "accounts",
        "ci"
      ]
    }
  }
}
```


## License

MIT © [Nicolas Gryman](http://ngryman.sh)


[commitizen]: https://github.com/commitizen/cz-cli
[Inquirer.js]: https://github.com/SBoudrias/Inquirer.js/
