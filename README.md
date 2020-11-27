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
https://download.eqdkp-plus.eu/repository.php?function=core_update&old=2.3.25&new=2.3.26
```

Response if a newer version is available:
```
{"info":"new core available","status":1}
```

Response:
```
{
   "link":"https:\/\/eqdkpcdn2.freetls.fastly.net\/core\/2.3.35_1\/Update_Packages\/eqdkp-plus_2.3.1_to_2.3.35_update.zip",
   "hash":"7c58f3b6c1a60607ab99b01c54a26ef4c489dc5d",
   "signature":"NoNxKJX639ky6+X\/ljfZ2DCIZPNXHKuWBgObCh2bxbimKbDWo\/kjXN4QJxbk1oLQLZTbKAVJfZNlao\/\/kANK6eBAAbX7ctkjLI1xc6z29k1pTewZBDVI64KymaddG5UkY\/x3r1HwhDgD8dXB9IFgqznQaZU+ISg+hUqad9vM0YdQshdRCy2H+l\/mE5o3MC\/iYKc5TSDECdyWJPYEClYVWDEforACPMTNAzW66lGi1UZ2olfbYhq\/hIWl+Wu65nP84M55tuOdR06cddtRj0npOLX4PbXUqYRSELbAb9gpeZe\/X92P6v5T1AY6FPwS19pLu9MbMIixtZBZyKTP3FUmSvFWkXJi58yNnHSVrHCfcEd4npnwLkBJeDzg\/MsPpu67IFcUGp8odxWyuhZ8rjSOUayqi8fQmiSD+ZyKdKZMiCOcGNIynCxQq\/j6Lumh9OrxXVDVC5KwHM2iVveHt3at5NokSgDPK5sbiN\/5JhobMOXJ2YRN+GXvRV+0T6kw5EPhA3UU67mFmHBX1UhGkhRSGItyvA0Xi+Um4RC7rD79zvjc8VW8AfIPZ6IjxFBkNAbVOsea7lcMpayzm9xVb6ZEeJLUg\/XgZO1\/N78Jdr+AEogrSqtF2hmQosepheFRcOyJnj5\/mgx\/eK6HasnGbWRoi2oL4slwVjip1O5WuMu4Hy4=",
   "new_version":"2.3.35.0",
   "releasenote":null,
   "hash_sha256":"2b0387652b5ace61e5f0e27440b643d3b8905945bc78d497c50b4583089cad03",
   "signature_sha256":"Cz3aMCOiw0r82SvrtOHC1A1zIHjeJqPAg2\/vl9NxrWdbM9oDrONmmr41Ajo2nEyRdins1H8u\/YQNwsD0XzkZs7MyN1RC2XaCzco0QWsHkfmSaQripg98KDc3W4mp+xP81w8n+P4j5kaudpx5ZAcnCHD7TZqwf5FJoSYWKjkAhgyYnlxdLBlh8ZFYIIZkxjJ+1fG2WUstN5BK2BM9u4RmHlvI8OBkKKu99dOqU95ZVzxVelhFTViqUITRDLgF3ebprGW5+KhDkDDdxEDecUEDQHfVEgE76+G7nJuZNgV5knXGGTTYrXpIiFwzVEBMRAEwHjdevOz2YxKtFGDvg6uYjfgRDJJeaOOYmePyGOaLQuyxdMyxtzqdsm1CerKAhExwrZ6w6gJDE9EfF+xE4xk1vf16RVFz8tZsnw2VsTA0YzxOMw3VTZC+JAE99T1wnVBzrPyKJ17csubGG4TdFT+mkvChXasnX1g2A93jvHArfLp+PHi8vTu5uT79um\/eSbjdLZdGqZYKDqMWOFw7U039zNbKHJtdmSYkspL9k4uCMLR+zRBtQTUW3jU\/03yjul5AXTHX7B1NudKO\/LKIaCELoHamPB9kULPnAMfCS+wVbdaq2Y\/DJOxGdqLt5QChq5KU7IVFZ0SGgpDfWRUHw5h5kCGW3qbJbxr4RoSCpie9SmU=",
   "status":1
}
```
The response contains a md5-hash (`hash`, legacy) and a sha256-hash (`hash_256`) of the Zip-File.
For the signatures, the algorithmns `sha1WithRSAEncryption` (legacy) and `sha256WithRSAEncryption` are used. See [misc-signer Repository](https://github.com/EQdkpPlus/misc-signer/) for implementations.

## Get Extension Download Link
Request:
```
https://download.eqdkp-plus.eu/repository.php?function=downloadid_link&id=229&core=2.3.36&category=1&name=SK%20Startorder
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
