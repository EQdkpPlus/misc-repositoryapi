# misc-repositoryapi
Repository API

## Fetch Extension-List
Request:
```
https://download.eqdkp-plus.eu/repository.php?function=extension_list&core=2.3.6.0
```
The request contains the current core version, so we can provide all extensions that fit to the core version

Response:
```
{
   "extensions":{
      "extension_229":{
         "plugin_id":229,
         "version":"1.0.4",
         "level":"stable",
         "name":"SK Startorder",
         "plugin":"sk_startorder",
         "changelog":"1.0.0\r\n- Initial Release",
         "releasedate":1512582080,
         "category":1,
         "author":"Godmod",
         "dep_coreversion":"2.1.0.9",
         "dep_coreversion_to":"2.3.999",
         "shortdesc":"Set the startorder of some SK Lootsystems.",
         "downloads":1010,
         "rating":0,
         "views":0,
         "dep_php":"5.4",
         "bugtracker_url":"",
         "tags":"a:1:{i:0;s:0:\"\";}"
      },
      "extension_565":{
         "plugin_id":565,
         "version":"2.2.10",
         "level":"stable",
         "name":"MediaCenter",
         "plugin":"mediacenter",
         "changelog":"2.2.9\r\n- Better display of notification titles",
         "releasedate":1591702170,
         "category":1,
         "author":"Godmod",
         "dep_coreversion":"2.3.0.17",
         "dep_coreversion_to":"2.3.999",
         "shortdesc":"Upload Images, Videos or Files to the MediaCenter. It combines a Gallery, Videosection and a Downloadsection. Also supports Videoplattforms like Youtube, Twitch or vid.me.",
         "downloads":2371,
         "rating":0,
         "views":0,
         "dep_php":"5.6",
         "bugtracker_url":"https:\/\/eqdkp-plus.eu\/bugtracker\/Product\/30-MediaCenter\/",
         "tags":"a:7:{i:0;s:6:\"images\";i:1;s:5:\"files\";i:2;s:8:\"download\";i:3;s:5:\"media\";i:4;s:6:\"plugin\";i:5;s:5:\"video\";i:6;s:7:\"youtube\";}"
      },
      "extension_694":{
         "plugin_id":694,
         "version":"0.2.4",
         "level":"stable",
         "name":"Warcraftlogs",
         "plugin":"warcraftlogs",
         "changelog":"0.2.4\r\n- Lazy Loading for Images\r\n\r\n0.2.3\r\n- Try to detect raidlogs by eventname\r\n\r\n0.2.0\r\n- Added classic APIs\r\n\r\n0.1.5\r\n- Added wowclassic to the supported games\r\n\r\n0.1.4\r\n- Fixed Boss Icons\r\n\r\n0.1.3\r\n- Fixed guildname",
         "releasedate":1594548140,
         "category":1,
         "author":"Godmod",
         "dep_coreversion":"2.3.0.24",
         "dep_coreversion_to":"2.3.999",
         "shortdesc":"This Plugins shows the boss fights at the raid details. Also, it comes with a portal module showing the latest logs from Warcraftlogs.com.",
         "downloads":3389,
         "rating":0,
         "views":0,
         "dep_php":"5.6",
         "bugtracker_url":"",
         "tags":"a:3:{i:0;s:3:\"wow\";i:1;s:4:\"logs\";i:2;s:12:\"warcraftlogs\";}"
      },
      "extension_pk":{
         "plugin_id":1,
         "version":"2.3.36.0",
         "level":"stable",
         "name":"EQdkp Plus Core",
         "plugin":"pluskernel",
         "changelog":"2.3.36\r\n- Fixed some Bugs",
         "releasedate":1604425171,
         "category":1,
         "author":"EQdkp Plus Dev Team",
         "dep_coreversion":"2.3.0.32",
         "shortdesc":"EQdkp Plus Core Version",
         "downloads":0,
         "rating":0,
         "views":0,
         "dep_php":"7.1",
         "bugtracker_url":"",
         "version_ext":"2.3.36"
      }
   },
   "status":1
}
```
The `extension_pk` (PK = Plus kernel) contains the information about the latest version of the EQdkp Plus core.

## Get Core Download Link
Request:
```
https://download.eqdkp-plus.eu/repository.php?function=core_update&old=2.3.25.0&new=2.3.26.0
```

Response if a newer version is available:
```
{"info":"new core available","status":1}
```

Response:
```
{
   "link":"https:\/\/eqdkpcdn2.freetls.fastly.net\/core\/2.3.36_1\/Update_Packages\/eqdkp-plus_2.3.30_to_2.3.36_update.zip",
   "hash":"731bf174fe52f0b80f9cb2e554444281270e8d38",
   "signature":"DIwm+a5UFKuIQS2+7ZiIjzuSK5oZmgPxV+et2seKfUXB\/NriauA++N46ThUc+l4WQjMbiqb4KLoeJH1AlFUMRMnrPlONaWD3RST7rzvZN2f3LPVq++rLMQqR2EaiNg+gZsps6gxl8DYFytEgvjcWhyNn0l6bsp3XnXzVOwOezH9scp8YbhdqVU8zIK+4P1TrTIqThxoupxdTZO5RH5Qm5w4NbDwZDe7be3WjY95MFDBw68B6Yw3aASNzitSr0K\/qvAJ7vaNGqH9QsnjIO9j1ad1hv1wJsmeGbgKfAYdQbTI258kO3\/0Jdfx8uuQusXRacVM8GWBt7\/XzDkLWmfVH22nLurimiaDK\/6tZmIv7blrI6yAT+WNk2LjhTqBCvG99JKVovv7mvlkewVLVAHF39tUZgLGwC8xIQ\/Ha+Kyy95\/P1t\/T1h+8IRWy4qOpqPpJRboJg51SgfXvqMhv6EEMv78jGLiQ7fAcU\/0AeI6dDiUOaIySkztwRB3cfZfPinIr3mlYo62bqB4C\/jgATzakncJqupIG27YwQS49IXvQrh3FMPN+SMHcZ7twWetz\/3dHeWE9PYnhcHlk+5tghSa34VhkvPJSFP8tIZIGC1ULLqS1MPjM8WzE0iODY56+5JdBkzkibPd7pru69gjoZnQTAsycmNoG6k4izWOrPDeLtlQ=",
   "new_version":"2.3.36.0",
   "releasenote":null,
   "hash_sha256":"1c002be42148c3d57027627df7e0072b75002b054aa4f293e939a33e13741d1a",
   "signature_sha256":"YVCHWJLSNNb0SIZYk7U\/6CN4UroJC0Q2jEbk+qJ7bKAke2mk8\/bXuUSt3w372eLpTQthT\/Vrn6wNEgTykNhreuabmFRMYLs+1HI32oUXOSvpdsd3G4sMGqDk1QSr1se8lVUzAZ5vVk4SGZEPs5G6wc5w6ok9WfFCyhNBnrJuDeQ2SAdA8uiDvEycn0+OBPBek97wrsx3LIsvj2L+tCzaQ0vTyMLYcqyhvDTovJp0BI08a99EOH9hJvLBZa7ZBbmP5cnySvqkeULXLsEOC718vzFm8snTscLQmfhCsOXSIYYFaMYYy7GMgCAV7RdPLD3Gt4pOEKcV3qhHwuHkNSW0P3MxflOUzdO8FBhGnIH8iE5ZHGN44T84R814zeSRGvGAQscEkG0UvFawUgn7+hPXxVJXjIAxsPBrAjaa4qlOLxI4Nz2+2vD7\/NDpZg7ReckgaxXdhjIG41M8nWSxI0U9g1cLdssswD6IEvZ1aOPZkKyZvzcp+nFMcwqaactHNiIS5yiktAIqfSdI0u4b0DcjfcWiwLUSlfX03uuhwCCH2EdfR0Us1Xb6Hw+9C7Plh5utVYzn5VZ4bA80zkmPyltdgbtd6jwKrR1eSnK4TxpePCw8zoVMgRu3qPByiQ9h98Zw+iRbt6840FL7k\/MmEnsnpzbs6+HUT0rlgEucXeJIPHs=",
   "status":1
}
```
The response contains a md5-hash (`hash`, legacy) and a sha256-hash (`hash_256`) of the Zip-File.
For the signatures, the algorithmns `sha1WithRSAEncryption` (legacy) and `sha256WithRSAEncryption` are used. See [misc-signer Repository](https://github.com/EQdkpPlus/misc-signer/) for implementations.

## Get Extension Download Link
Request:
```
https://download.eqdkp-plus.eu/repository.php?function=downloadid_link&id=229&core=2.3.36.0&category=1&name=SK%20Startorder
```
* `id`: the extension ID
* `core`: the current core version
* `category`: the numeric category ID. 1 = plugin, 2 = template, 3 = portal, 7 = game, 11 = language
* `name`: the name of the extension

Response:
```
{
   "link":"https:\/\/eqdkpcdn2.freetls.fastly.net\/plugins\/sk_startorder_1.0.4_42bbb13.zip",
   "hash":"2688f7c7cd259c86ed46cb270e8349680f756364",
   "signature":"XAvhRT3A1vvODrYU0CisiAqRrrLT+IR5uq6K5\/NUsN3rp3mo2IuoukBDmF2DsHqb7bN38p0jSCETxRvGjPimxaAFwG+gTAc7kRqRy23hZNX3mEbW7H7pNlUNH2+ZQrAs38aQ92DyR6O+zLtY00RRK0p\/Cw02cGco6j23De1bQYyMXLFNottgU20\/+HBXefgKkZCFk7IGx05FI9uWsG5PGs0VwLpqUL06HuzbMns0rDAqHBYqLXncNt+H\/g7+4J4XTXZs9wS9\/OOa66ziLNRagP\/BYwBKkkHQjyC5snUDFjXQ6BG3gjEWn7iib\/K9F3zrU967JDedSWqlZobxcr7u3EwzAdvTUp3rEGBDetZ+z8i9g+erM66X4X0L7kO6R6987EOhTW7F5kM1SOMNX7bui\/GQrpDsq4\/xi8YOVyswOuoOG9As0luXAdvXwM5WrDph0Zv21eqNT4TkbRupHvedCbmBoU\/P\/9tMtJG5nIQTud27GTkIBoG+ifigPj58G+vr\/aAxoZPv9cLrr9oZojhmwrn0KuQlhLEUEQxaet9WP\/sdyT8FY6Ejjz9GCTo0jUYE0IXnZiOFo6xv2fqOK84q\/YEpbqfQPvSLh31KOd5d8W2HZCZTUMcadsvlLi8DEvV3IrhX+bOJQ0skyCkuWt8V+Z7ORlQTzf8cNjYnjtAs7Lg=",
   "hash_sha256":"c541f2897973b6ac339758a3beff9697d89564936c9a720008f4ce97646c8a77",
   "signature_sha256":"icrzIstw0T1O9G6a5OMNLRNIFX9jrDPF+Gw1MDbfmnqlg1ZMCIyiOuKaZE1hy0JpZ5+glHNu9P6AgucoBaQjGzUjHomzOnkbd76y2rNupv1suIPTRUgJnHsicm5BMXGt0nB7\/VkMlA0unMAc50j7ZHmRohGiA4f0sz7Q+jvkTHMj9+G2pjRpIP\/ztDta6xHVK\/87iFFH9wiBLGaoGQ\/hsmuyJt1sIhiMDQXwopUz362deTLNPC2\/GHal8ALg9AWHAGjQipV0DRYZsosVjdAhtzsi8lSLhrjBLhQeObzPPZMYdgMOthDvWeLa9tGgJVpZ46H2CVW0Ieenx2wNi2hSAcZvUxYCR+rl4zVGMT2rm1va7ko2C30DYhcnzeT63rmjjNGqBBeKSLh5gx2V4ezxDkPa5M8Sgz2mgweTuaIHhFnfel8MxATsu6Y\/6IzE6ZSmue44lV24H0lYAf2F9JR68Sl9rpi9qJSiyAPMdkTmonOInmMAORquJ4bypMNBzpk+NiB\/ETcQMKjkxbjO3IXh88tOc1grGqi6yxwYDdatsLcUSLf6\/WhNDZRJU+279iaQP7QeIcho7gBjacLHuvjxVlDWN28vkxqU\/R4jiblPB1wchiayGk8J6YfwO9i+f88gsG0E2XFo7cYYZH\/jDaAcwNmeSgPh6OFXX1NLPig4PNg=",
   "status":1
}
```
The response contains a md5-hash (`hash`, legacy) and a sha256-hash (`hash_256`) of the Zip-File.
For the signatures, the algorithmns `sha1WithRSAEncryption` (legacy) and `sha256WithRSAEncryption` are used. See [misc-signer Repository](https://github.com/EQdkpPlus/misc-signer/) for implementations.

## Get Intermediate Certificates
Request:
```
https://download.eqdkp-plus.eu/repository.php?function=interm_cert
```
Response:
```
{
   "cert":"\/\/EQdkp Plus Core Intermediate 2020\n-----BEGIN CERTIFICATE-----\nMIIDsjCCAxugAwIBAgIBEjANBgkqhkiG9w0BAQ0FADAtMRMwEQYDVQQKEwpFUWRr\ncCBQbHVzMRYwFAYDVQQLEw1FUWRrcCBQbHVzIENBMB4XDTE5MTIyNzE1MTEwMFoX\nDTIxMDEyMjE1MTEwMFowLzETMBEGA1UEChMKRVFka3AgUGx1czEYMBYGA1UECxMP\nRVFka3AgUGx1cyBDb3JlMIICIjANBgkqhkiG9w0BAQEFAAOCAg8AMIICCgKCAgEA\nnypPsOs2anXREqsmpVV35zhs1DCXhiCAkA\/0O5b1Pd0hTAhG4jhscdOOZh5HfY6U\ntYUt1ayxgS0OJn6IMThNwP0XlHXZe1QSpuREFFJ3EoJXm888ALavUiJqX9GA3Lt0\nKCqRVIZjmESegZKNWT3FTfuLb6qLY3SSkzLWPNkaGl4\/i7ORmChfXGoinC+VYniU\nrzEpMszuxqZyBoczjFbQe8pdWx0XPkRx5qw0sCfp0vzhmua6iNo3grHQZx26VZQM\ncTN8BgCrFteJIHIuGrwo1+E+wsvIkyGoKOLv2d7Jr6YBBHkUtbBpMuGpPL40PozB\nmUyT4nlrIPC83wBfMTja2rlMCqN5QwxMR3rnS0tc2LCZIK2dO8GiHFlauNz5+5An\nS5dbSFuBSwlt65s3vae\/D8T8SgysCCM9xBS20Ld7h6Whose8ceFhzS6qK3hAZwKn\nQRtCo34BtkhZf8Y6BXo+JN6weBjjmjg3PSt05Efoe\/b5gx23dh1wZP7eiVxMlCW3\n2bdJzhH9ZSMLeDRoi+4r49EIehnGpL\/ehLOIFYZgeRaSNzqQCZfEouVAjc2\/e\/w3\nTD8iQADqCBmGDDu7jK\/aeIlDdwvOl68mf29V9ZMBgDwNFuL0I307B18Re44CZxpJ\nAZZmAuheEa2zM6DASa\/Ed8rAJ0RRvOHkBq09xUoXGMECAwEAAaNcMFowDAYDVR0T\nAQH\/BAIwADAdBgNVHQ4EFgQU90hz2EhH0f4w+5cOahryDsim9RAwCwYDVR0PBAQD\nAgeAMB4GCWCGSAGG+EIBDQQRFg94Y2EgY2VydGlmaWNhdGUwDQYJKoZIhvcNAQEN\nBQADgYEAJ69UVfU9kIpOY+xTylcVwD5Q8XHQwd4wJoc7qKjtzR4aGgDoRL5MGGDO\njCTrBXRKISi3oFuBWv6tARwaCjrjDxiehdH8BoI2MtxTlEnRqxemLMO+MyQ74CHa\nDSkWiSklOhSIpJnkut0BFzZHu3+blDZv7Xh8XhVGeSNgM2eTUp8=\n-----END CERTIFICATE-----\n\n\/\/Asitara Dev 2020\n-----BEGIN CERTIFICATE-----\nMIIDvTCCAyagAwIBAgIBMDANBgkqhkiG9w0BAQ0FADAzMRMwEQYDVQQKEwpFUWRr\ncCBQbHVzMRwwGgYDVQQLExNFUWRrcCBQbHVzIFBhY2thZ2VzMB4XDTE5MTIyNzE1\nMTgwMFoXDTIxMDEyMjE1MTgwMFowNDETMBEGA1UEChMKRVFka3AgUGx1czEdMBsG\nA1UECxMURVFka3AgUGx1cyBEZXZlbG9wZXIwggIiMA0GCSqGSIb3DQEBAQUAA4IC\nDwAwggIKAoICAQDI+o6rYu1Xyf5BjhRu9yF43g2N5AmDVcW\/D0vTIQKpDlzmwxzI\nFEd3VwiAItmV1xw74VMNYxfEa2VXzV857Bxt+St2+XxPEqxQzMvI6pF70xLtgqFe\nLvIEwehUfC0LKOywCogt2P4QsmkH9Vz3FeLfTjsV5iNj9\/FVw5j0wHIg2m3qQfVO\n6H4lkmwaISZRZzjQwoeLtmfZXBRICkJL0Vdepdt7xndeDSxzkyiSGE\/RvVRut+Hm\neQH4lTGMxvRB\/csZxk7d2d3O8qZU+\/UG0xAqhKWYAOnY\/JDnhh+pZlqVyJ+26gy8\nFIrFWzKIXBo7DE8dMkvU1V9mak4mquQstKJud4supV1kW5U529AAHHn0scOjkoYX\nKljoGOZomKuLhWGG1zN3FELRzsUi28C4b+ZVVX6muaeKhD\/4rBxc5lbuH6Tycwl\/\nWNLrcCjjgkjSfWd66fzxaQHdgdaBoqWyqdmMMUq4WZKbhFTybdQYvOov\/pJVvqmK\nhFSyudca9n07KlAF5RPVEdGFLFT5rJelce1s\/e6eYcnlHafEwuLU0lBTY6a++szm\ntG6nXtZa0GGsjBmdoo6AmFTNVLEc+OEDb8Z1WoVDJyyNw+va85HYpuHpJh8FoND9\n06R\/eOY9U1SzYk5whW6iFpps1Gb\/nfKrkqgSfXaj63EVqpZtsESS\/fqaEwIDAQAB\no1wwWjAMBgNVHRMBAf8EAjAAMB0GA1UdDgQWBBSeLweun2L9P7a6wz90xDG7HYYS\nljALBgNVHQ8EBAMCB4AwHgYJYIZIAYb4QgENBBEWD3hjYSBjZXJ0aWZpY2F0ZTAN\nBgkqhkiG9w0BAQ0FAAOBgQALgkrEEayZwEPtdkJKGs\/vKFIztvNbKFQK3jJpyCI9\nsVPKuGIViSA6dtmtr9MiT86WJq444QGYc9UXse6cK6RQTwn7XkftNpCTeHnqVaHa\nbMwM3pWa0Wb5CPVKaEJ2CylctGtJyuUm9LuuZEC3YP4a6agAjjkc5n+yYRnAGKFk\n6w==\n-----END CERTIFICATE-----",
   "status":1
}
```
