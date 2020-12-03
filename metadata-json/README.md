# Nasjonalmuseet collection metadata (03.12.2020)

Export in JSON from Elastic 7.8.1 via Postman, using Elastic Scroll API:
https://www.elastic.co/guide/en/elasticsearch/reference/6.8/search-request-scroll.html

**42 465 objects**

5 json files (4 x 10,000 + 1 x 2,465).

Only collection objects with multimedia/photo are included.
Some objects have more than one photo included in the dataset. The main/default photo can be identified by the parameter `"Thumbnail": true` in the `Multimedia` part of the metadata.

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

Please note that around 10 000 collection objects are still in copyright. The photo license for all other objects is CC-BY-4.0.

## Full object example (Edvard Munch, _Scream_)
https://www.nasjonalmuseet.no/samlingen/objekt/NG.M.00939
```javascript
{
    "_index": "nm-prod-collection-object-no",
    "_type": "_doc",
    "_id": "34275",
    "_score": 1.0,
    "_source": {
        "MetaData": {
            "OrgUnit": [
                "Billedkunstsamlingene"
            ],
            "AccessionTypeNMK": [
                "Ervervelse"
            ],
            "Owner": [
                {
                    "FullName": "Nasjonalmuseet for kunst, arkitektur og design",
                    "PersonType": [
                        "Institusjon"
                    ],
                    "Id": "47704",
                    "LastName": [
                        "Nasjonalmuseet for kunst, arkitektur og design"
                    ],
                    "UrlSegment": "nasjonalmuseet-for-kunst-arkitektur-og-design"
                }
            ],
            "BarcodeNumber": [
                "G-34275"
            ],
            "Keywords": [
                "Bildende kunst"
            ],
            "Materials": [
                "Papplate"
            ],
            "IsArtwork": [
                true
            ],
            "CataloguingLevel": [
                "Enkeltobjekt"
            ],
            "ObjectTitle": [
                {
                    "Type": "",
                    "Title": "Skrik",
                    "Alternatives": [
                        {
                            "Title": "The Scream",
                            "Lang": "ENG"
                        }
                    ]
                }
            ],
            "ObjectType": [
                "Billedkunst"
            ],
            "SubjectType": [
                "Landskap",
                "Portrett"
            ],
            "Copyrights": [
                {
                    "PersonManagerRef": 0,
                    "PersonRef": 56154,
                    "PersonRefMetaData": {
                        "FirstName": [
                            "Edvard"
                        ],
                        "FullName": "Edvard Munch",
                        "PersonType": [
                            "Person"
                        ],
                        "Id": "56154",
                        "LastName": [
                            "Munch"
                        ],
                        "UrlSegment": "edvard-munch"
                    },
                    "CopyrightsStatus": "Inaktiv",
                    "DateTo": "2014-01-23T00:00:00Z"
                }
            ],
            "Classification": [
                "532 - Bildende kunst"
            ],
            "Production": [
                {
                    "ProductionType": "Produsert",
                    "LevelCertainty": "sikker",
                    "PersonRef": 56154,
                    "DateToBegin": "1893-01-01T00:00:00Z",
                    "DateFromEnd": "1893-12-31T00:00:00Z",
                    "DateFrom": "1893",
                    "DateFromBegin": "1893-01-01T00:00:00Z",
                    "PerRole": "Kunstner",
                    "PersonRefMetaData": {
                        "FirstName": [
                            "Edvard"
                        ],
                        "FullName": "Edvard Munch",
                        "PersonType": [
                            "Person"
                        ],
                        "Id": "56154",
                        "LastName": [
                            "Munch"
                        ],
                        "UrlSegment": "edvard-munch"
                    },
                    "PlaceRef": 0,
                    "DateToEnd": "1893-12-31T00:00:00Z",
                    "DateTo": "1893"
                }
            ],
            "SubjectRelatedPersons": [],
            "Multimedia": [
                {
                    "Photocredit": [
                        "Høstland, Børre"
                    ],
                    "LastModified": [
                        "2019-07-18T13:46:04.6010000"
                    ],
                    "Usage": [
                        "Standard-bilde"
                    ],
                    "ImageDimensions": {
                        "Height": "4000",
                        "Width": "3223"
                    },
                    "Id": 47488,
                    "MultimediaType": [
                        "Fotostation"
                    ],
                    "Thumbnail": true,
                    "OriginalFile": [
                        "113298.tif"
                    ],
                    "DocumentName": [
                        "D:/FSStorage/bfiles/hel/hel_006/113298.jpg"
                    ],
                    "Created": [
                        "2019-07-18T13:46:04.6010000"
                    ]
                },
                {
                    "LastModified": [
                        "2019-07-18T13:51:42.4290000"
                    ],
                    "Usage": [
                        "Detaljbilde"
                    ],
                    "ImageDimensions": {
                        "Height": "1495",
                        "Width": "2000"
                    },
                    "Id": 43925,
                    "MultimediaType": [
                        "Fotostation"
                    ],
                    "Thumbnail": false,
                    "OriginalFile": [
                        "54318.tif"
                    ],
                    "DocumentName": [
                        "D:/FSStorage/bfiles/003/54318.jpg"
                    ],
                    "Created": [
                        "2019-07-18T13:51:42.4290000"
                    ]
                },
                {
                    "LastModified": [
                        "2019-07-18T13:51:42.4290000"
                    ],
                    "Usage": [
                        "Detaljbilde"
                    ],
                    "ImageDimensions": {
                        "Height": "1495",
                        "Width": "2000"
                    },
                    "Id": 45775,
                    "MultimediaType": [
                        "Fotostation"
                    ],
                    "Thumbnail": false,
                    "OriginalFile": [
                        "54321.tif"
                    ],
                    "DocumentName": [
                        "D:/FSStorage/bfiles/003/54321.jpg"
                    ],
                    "Created": [
                        "2019-07-18T13:51:42.4290000"
                    ]
                },
                {
                    "LastModified": [
                        "2019-07-18T13:51:42.4290000"
                    ],
                    "Usage": [
                        "Detaljbilde"
                    ],
                    "ImageDimensions": {
                        "Height": "2000",
                        "Width": "1511"
                    },
                    "Id": 46848,
                    "MultimediaType": [
                        "Fotostation"
                    ],
                    "Thumbnail": false,
                    "OriginalFile": [
                        "54319.tif"
                    ],
                    "DocumentName": [
                        "D:/FSStorage/bfiles/003/54319.jpg"
                    ],
                    "Created": [
                        "2019-07-18T13:51:42.4290000"
                    ]
                },
                {
                    "LastModified": [
                        "2019-07-18T13:51:42.4290000"
                    ],
                    "Usage": [
                        "Detaljbilde"
                    ],
                    "ImageDimensions": {
                        "Height": "2000",
                        "Width": "1511"
                    },
                    "Id": 47243,
                    "MultimediaType": [
                        "Fotostation"
                    ],
                    "Thumbnail": false,
                    "OriginalFile": [
                        "54320.tif"
                    ],
                    "DocumentName": [
                        "D:/FSStorage/bfiles/003/54320.jpg"
                    ],
                    "Created": [
                        "2019-07-18T13:51:42.4290000"
                    ]
                }
            ],
            "ObjectNumber": [
                "NG.M.00939"
            ],
            "MaterialTechnique": [
                "Tempera og fettstift på papplate"
            ],
            "TechniqueDecoration": [],
            "Dimensions": [
                {
                    "DimensionsType": "Bredde",
                    "DimSizeUnit": "cm",
                    "DimensionsCategory": "Hovedmål",
                    "DimensionNum": 73.5
                },
                {
                    "DimensionsType": "Høyde",
                    "DimSizeUnit": "cm",
                    "DimensionsCategory": "Hovedmål",
                    "DimensionNum": 91.0
                },
                {
                    "DimensionsType": "Bredde",
                    "DimSizeUnit": "cm",
                    "DimensionsCategory": "Rammemål",
                    "DimensionNum": 95.0
                },
                {
                    "DimensionsType": "Dybde",
                    "DimSizeUnit": "cm",
                    "DimensionsCategory": "Rammemål",
                    "DimensionNum": 6.5
                },
                {
                    "DimensionsType": "Høyde",
                    "DimSizeUnit": "cm",
                    "DimensionsCategory": "Rammemål",
                    "DimensionNum": 113.1
                }
            ],
            "ProductionLocations": [],
            "SubjectRelatedPlacesParsed": [],
            "PublicDomain": [
                true
            ],
            "ObjectName": [
                "Maleri"
            ],
            "Creditline": [
                "Gave fra Olaf Schou 1910"
            ],
            "Technique": [
                "Tempera",
                "Fettstift"
            ],
            "SubjectRelatedPlace": [],
            "PreviewDimensionsNo": [
                "91 x 73,5 cm"
            ],
            "Labeldate": [
                "1893"
            ]
        },
        "NmId": "NG.M.00939"
    }
}
```

