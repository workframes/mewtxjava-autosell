# MewtXJava Autosell

> What is it?
- It gathers all the UGC Limiteds you have and sells all the one that are out of its holding period according to your settings.

## Credits 
- [Mewt](https://discord.gg/mewt)
- [Java](https://discord.gg/javaw)

## Requirements
- [Python](https://www.python.org/downloads/)
- [requests](https://pypi.org/project/requests/)
- [colorama](https://pypi.org/project/colorama/)
- [rgbprint](https://pypi.org/project/rgbprint/)

## Disclaimer
If you do plan on using this, and if something goes wrong and you loose robux. You will not be refunded as you are using this by your own choice.

## Installation
Grab the latest version from [here](https://github.com/workframes/mewtxjava-autosell/releases)
If you are running this on `Mac OS` run it using `main.py`, if you are running it on `Windows` you can run it with either `start.bat` or `main.py`

## Settings Documentaion
- `COOKIE`
    * The `.ROBLOXSECURITY` of the acount you want to sell items on.
- `SELL_METHOD`
    * What sell method you want to use, here are the following options and what it does.
        * `MEWTVALUES` 
            * Sells your items according to the valuation generated by mewt.
        * `UNDERCUT`
            * Sells your item for 1 robux under the most recent price. It will constantly update the price to 1 robux under as well every 5 minutes.
        * `CUSTOM`
            * Sells your items according to the prices you set in `CUSTOM_VALUES`. 
- `MEWTVALUE_MULTIPLIER`
    * If you are using the `MEWTVALUES` sell method you can use this to multiply the valuation made by mewt before putting up for sale. This value will always be 1 or greater. Example: An item with the value of `40` with the multiplier of `1.23` will be sold for `49` because `40 * 1.23` is about `49` or to be exact `49.2`.
- `CUSTOM_VALUES`
    * These are the custom prices that will be used to for the sell method `CUSTOM` While using this only the items included in custom values will be resold. Example:
        * ```json
            "CUSTOM_VALUES": {
                "13345169760": 40
            }
            ```
- `WHITELIST`
    * It will **ONLY** resell only the items listed in there, it will apply for all selling methods and will also follow the `BLACKLIST`
- `BLACKLIST` 
    * If a item is in this list, it will not put it up for resale.
- `WEBHOOK`
    * If you have this enabled it will send notfications when a item sells.
    - `ENABLED`
        * `true` to enabled the feature
        * `false` to disable the feature
    - `URL`
        * If you have enabled you must have a discord webhook.
## Example Settings
```json
{
    "SELL_METHOD": "CUSTOM",
    "SELL_METHOD": "UNDERCUT",
    "MEWTVALUE_MULTIPLIER": 1,
    "CUSTOM_VALUES": {
        "13599801260": 60
    },
    "WHITELIST":[
        13345169760
    ],
    "BLACKLIST": [
        13636293210
    ],
    "WEBHOOK": {
        "ENABLED": true,
        "URL": "https://discord.com/api/webhooks/abc/abc"
    }
}
```

## Still having toruble?
* Join one of the discord servers mentioned in [Credits](https://github.com/workframes/mewtxjava-autosell#credits) and they will be happy to help you!