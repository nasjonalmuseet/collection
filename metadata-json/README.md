# JSON export from Nasjonalmuseet collection (Elastic 7.8.1) 03.12.2020*

Export via Postman, using Elastic Scroll API:
https://www.elastic.co/guide/en/elasticsearch/reference/6.8/search-request-scroll.html

**42 465 objects**
5 json files, 10000x4 + 2465.
Only objects with multimedia/images are included.
Some objects that have more than one photo included in the dataset. The main/default photo can be identified by the parameter `"Thumbnail": True` in the `Multimedia` part of the metadata. The image identifier is found in the `Multimedia.OriginalFile` value.

**Example**
```javascript
"Multimedia": [
               {
                "LastModified": [
                    "2019-07-18T13:51:42.5080000"
                ],
                "Usage": [
                    "Standard-bilde"
                ],
                "ImageDimensions": {
                    "Height": "1924",
                    "Width": "3000"
                },
                "Id": 32124,
                "MultimediaType": [
                    "Fotostation"
                ],
                "Thumbnail": true,
                "OriginalFile": [
                    "59037.tif"
                ],
                "DocumentName": [
                    "D:/FSStorage/bfiles/003/59037.jpg"
                ],
                "Created": [
                    "2019-07-18T13:51:42.5080000"
                ]
            }
           ]
```                           
To construct the url for the IIIF image resource, use the value of `OriginalFile` like this (for `"OriginalFile": "59037.tif"`):

JPG at 800px width: `https://ms01.nasjonalmuseet.no/iip/?iiif=/tif/59037.tif/full/800,/0/default.jpg`

IIIF info.json: `https://ms01.nasjonalmuseet.no/iip/?iiif=/tif/59037.tif/info.json`

Please note that around 10 000 images are still in copyright. The photo license for all other images is CC-BY-4.0.
