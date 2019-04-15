# heroku-buildpack-nano

Heroku buildpack that installs Nano text editor

## How it works

Installs Nano Ninja version from [Ehryk's](https://github.com/Ehryk) repository [heroku-nano](https://github.com/Ehryk/heroku-nano/) or if you prefer you can set a config var to download Nano from a custom location.

Nano installation ends in `/app/nano` directory.

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

## License

MIT © [Velizar Nenov](https://github.com/velizarn)