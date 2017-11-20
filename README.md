# homebridge-chamberlain

A Homebridge plugin for Chamberlain garage door openers with MyQ.

First set up your mychamberlain.com account, then add to your `config.json` in
the `accessories` array:

```json
{
  "accessory": "Chamberlain",
  "name": "Garage Door",
  "username": "your mychamberlain.com email",
  "password": "your mychamberlain.com password"
}
```

If you have multiple garage doors, the plugin will throw an error and list the controllable device IDs. Use those IDs to create individual accessories...
If one of the devices is a MyQ Light adapter, just pass "isLight": true so it is not treated as a garage door

```json
{
  "accessory": "Chamberlain",
  "name": "Main Garage Door",
  "username": "your mychamberlain.com email",
  "password": "your mychamberlain.com password",
  "deviceId": "xxx",
  "isLight": true
},
{
  "accessory": "Chamberlain",
  "name": "Side Garage Door",
  "username": "your mychamberlain.com email",
  "password": "your mychamberlain.com password",
  "deviceId": "xxx",
  "isLight": false
},
...
```
