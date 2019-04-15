# heroku-buildpack-nano

Heroku buildpack that installs Nano text editor

## How it works

Installs Nano Ninja version from [Ehryk's](https://github.com/Ehryk) repository [heroku-nano](https://github.com/Ehryk/heroku-nano/) or if you prefer you can set a config var to download Nano from a custom location.

Nano installation ends in `/app/nano` directory.

### Example usage

    -----> Build succeeded!
    -----> heroku-buildpack-nano app detected
        -> Custom nano URL is not set, start downloading from default location
        -> Downloading Nano... (https://github.com/Ehryk/heroku-nano/raw/master/heroku-nano-2.5.1/nano.tar.gz)
        -> Installing Nano...
        DONE
    -----> Discovering process types

## Configure from CLI

```bash
heroku buildpacks:add https://github.com/velizarn/heroku-buildpack-nano
```

## Configure from app manifest

```json
{
    "buildpacks": [
        {
            "url": "https://github.com/velizarn/heroku-buildpack-nano"
        }
    ]
}
```

### Add custom download location

If you prefer to deploy your own nano archve you can set a config var to download Nano from a custom location, e.g.

```bash
heroku config:set NANO_URL_CUSTOM=https://your-custom-url.domain.tld/nano.tar.gz
```

#### Example usage

    -----> Build succeeded!
    -----> heroku-buildpack-nano app detected
        -> Downloading Nano... (https://mycustomurl.rackcdn.com/nano-2.5.1.tar.gz)
        -> Installing Nano...
        DONE
    -----> Discovering process types

## Resources

- [Heroku Buildpack API](https://devcenter.heroku.com/articles/buildpack-api)
- [Heroku Configuration and Config Vars](https://devcenter.heroku.com/articles/config-vars)
- [Edit a File on Heroku Dynos using Nano or Vim](http://www.compulsivecoders.com/tech/how-to-edit-a-file-on-heroku-dynos-using-nano-or-vim/)
- [Nano editor homepage](https://www.nano-editor.org/)
- [Nano shortcuts](https://www.nano-editor.org/dist/latest/cheatsheet.html)

## License

MIT © [Velizar Nenov](https://github.com/velizarn)
