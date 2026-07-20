# Auphonic: Get API Information

Retrieves API information from Auphonic.

```
GET https://connect.mindcloud.co/v1/universal/auphonic/latest/actions/get-api-information
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Auphonic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/auphonic/latest/actions/get-api-information?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/auphonic/latest/actions/get-api-information?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "algorithms": {
        "backforeground": {
          "defaultValue": 1,
          "description": "string",
          "displayName": "Ava Chen",
          "options": [
            {
              "displayName": 1,
              "value": "string"
            }
          ],
          "type": "string"
        },
        "backgroundgain": {
          "belongsTo": "string",
          "defaultValue": 1,
          "displayName": "Ava Chen",
          "options": [
            {
              "displayName": 1,
              "value": 1
            }
          ],
          "type": "string"
        },
        "compressor": {
          "belongsTo": "string",
          "defaultValue": "string",
          "displayName": "Ava Chen",
          "options": [
            {
              "displayName": "Ava Chen",
              "value": "string"
            }
          ],
          "type": "string"
        },
        "compressorM": {
          "belongsTo": "string",
          "defaultValue": 1,
          "displayName": "Ava Chen",
          "options": [
            {
              "displayName": "Ava Chen",
              "value": "string"
            }
          ],
          "type": "string"
        },
        "coughCutter": {
          "belongsTo": "string",
          "defaultValue": true,
          "description": "string",
          "displayName": "Ava Chen",
          "type": "string"
        },
        "crossgate": {
          "defaultValue": true,
          "description": "string",
          "displayName": "Ava Chen",
          "type": "string"
        },
        "cutMode": {
          "belongsTo": "string",
          "defaultValue": 1,
          "description": "string",
          "displayName": "Ava Chen",
          "options": [
            {
              "displayName": "Ava Chen",
              "value": "string"
            }
          ],
          "type": "string"
        },
        "cutter": {
          "defaultValue": true,
          "description": "string",
          "displayName": "Ava Chen",
          "type": "string"
        },
        "debreathamount": {
          "belongsTo": "string",
          "defaultValue": 1,
          "displayName": "Ava Chen",
          "options": [
            {
              "displayName": "Ava Chen",
              "value": 1
            }
          ],
          "type": "string"
        },
        "dehum": {
          "belongsTo": "string",
          "defaultValue": 1,
          "displayName": "Ava Chen",
          "options": [
            {
              "displayName": "Ava Chen",
              "value": 1
            }
          ],
          "type": "string"
        },
        "dehumamount": {
          "belongsTo": "string",
          "defaultValue": 1,
          "displayName": "Ava Chen",
          "options": [
            {
              "displayName": "Ava Chen",
              "value": 1
            }
          ],
          "type": "string"
        },
        "denoise": {
          "defaultValue": true,
          "description": "string",
          "displayName": "Ava Chen",
          "type": "string"
        },
        "denoiseamount": {
          "belongsTo": "string",
          "defaultValue": 1,
          "displayName": "Ava Chen",
          "options": [
            {
              "displayName": "Ava Chen",
              "value": 1
            }
          ],
          "type": "string"
        },
        "denoisemethod": {
          "belongsTo": "string",
          "defaultValue": 1,
          "displayName": "Ava Chen",
          "options": [
            {
              "displayName": "Ava Chen",
              "value": "string"
            }
          ],
          "type": "string"
        },
        "dualmono": {
          "belongsTo": "string",
          "defaultValue": true,
          "displayName": "Ava Chen",
          "type": "string"
        },
        "duckingFadetime": {
          "belongsTo": "string",
          "defaultValue": 1,
          "displayName": "Ava Chen",
          "options": [
            {
              "displayName": 1,
              "value": 1
            }
          ],
          "type": "string"
        },
        "fillerCutter": {
          "belongsTo": "string",
          "defaultValue": true,
          "description": "string",
          "displayName": "Ava Chen",
          "type": "string"
        },
        "filtering": {
          "defaultValue": true,
          "description": "string",
          "displayName": "Ava Chen",
          "type": "string"
        },
        "filtermethod": {
          "belongsTo": "string",
          "defaultValue": 1,
          "displayName": "Ava Chen",
          "options": [
            {
              "displayName": "Ava Chen",
              "value": "string"
            }
          ],
          "type": "string"
        },
        "gain": {
          "belongsTo": "string",
          "defaultValue": 1,
          "displayName": "Ava Chen",
          "options": [
            {
              "displayName": 1,
              "value": 1
            }
          ],
          "type": "string"
        },
        "gate": {
          "defaultValue": true,
          "description": "string",
          "displayName": "Ava Chen",
          "type": "string"
        },
        "leveler": {
          "defaultValue": true,
          "description": "string",
          "displayName": "Ava Chen",
          "type": "string"
        },
        "levelerstrength": {
          "belongsTo": "string",
          "defaultValue": 1,
          "displayName": "Ava Chen",
          "options": [
            {
              "displayName": "Ava Chen",
              "value": 1
            }
          ],
          "type": "string"
        },
        "levelerstrengthM": {
          "belongsTo": "string",
          "defaultValue": 1,
          "displayName": "Ava Chen",
          "options": [
            {
              "displayName": "Ava Chen",
              "value": 1
            }
          ],
          "type": "string"
        },
        "loudnessmethod": {
          "belongsTo": "string",
          "defaultValue": "string",
          "displayName": "Ava Chen",
          "options": [
            {
              "displayName": "Ava Chen",
              "value": "string"
            }
          ],
          "type": "string"
        },
        "loudnesstarget": {
          "belongsTo": "string",
          "defaultValue": 1,
          "displayName": "Ava Chen",
          "options": [
            {
              "displayName": "Ava Chen",
              "value": 1
            }
          ],
          "type": "string"
        },
        "maxlra": {
          "belongsTo": "string",
          "defaultValue": 1,
          "displayName": "Ava Chen",
          "options": [
            {
              "displayName": "Ava Chen",
              "value": 1
            }
          ],
          "type": "string"
        },
        "maxm": {
          "belongsTo": "string",
          "defaultValue": 1,
          "displayName": "Ava Chen",
          "options": [
            {
              "displayName": "Ava Chen",
              "value": 1
            }
          ],
          "type": "string"
        },
        "maxpeak": {
          "belongsTo": "string",
          "defaultValue": 1,
          "displayName": "Ava Chen",
          "options": [
            {
              "displayName": "Ava Chen",
              "value": 1
            }
          ],
          "type": "string"
        },
        "maxs": {
          "belongsTo": "string",
          "defaultValue": 1,
          "displayName": "Ava Chen",
          "options": [
            {
              "displayName": "Ava Chen",
              "value": 1
            }
          ],
          "type": "string"
        },
        "msclassifier": {
          "belongsTo": "string",
          "defaultValue": 1,
          "displayName": "Ava Chen",
          "options": [
            {
              "displayName": "Ava Chen",
              "value": "string"
            }
          ],
          "type": "string"
        },
        "musicCutter": {
          "belongsTo": "string",
          "defaultValue": true,
          "description": "string",
          "displayName": "Ava Chen",
          "type": "string"
        },
        "musicgain": {
          "belongsTo": "string",
          "defaultValue": 1,
          "displayName": "Ava Chen",
          "options": [
            {
              "displayName": "Ava Chen",
              "value": 1
            }
          ],
          "type": "string"
        },
        "normloudness": {
          "defaultValue": true,
          "description": "string",
          "displayName": "Ava Chen",
          "type": "string"
        },
        "pan": {
          "belongsTo": "string",
          "defaultValue": 1,
          "displayName": "Ava Chen",
          "options": [
            {
              "displayName": "Ava Chen",
              "value": "string"
            }
          ],
          "type": "string"
        },
        "segments": {
          "description": "string",
          "displayName": "Ava Chen",
          "type": "string"
        },
        "silenceCutter": {
          "belongsTo": "string",
          "defaultValue": true,
          "description": "string",
          "displayName": "Ava Chen",
          "type": "string"
        }
      },
      "fileEndings": {
        "aac": [
          "string"
        ],
        "alac": [
          "string"
        ],
        "audiogram": [
          "string"
        ],
        "chaps": [
          "string"
        ],
        "cutList": [
          "string"
        ],
        "descr": [
          "string"
        ],
        "flac": [
          "string"
        ],
        "image": [
          "string"
        ],
        "input": [
          "string"
        ],
        "mp3": [
          "string"
        ],
        "mp3Vbr": [
          "string"
        ],
        "opus": [
          "string"
        ],
        "pod2chaps": [
          "string"
        ],
        "psc": [
          "string"
        ],
        "speech": [
          "string"
        ],
        "stats": [
          "string"
        ],
        "subtitle": [
          "string"
        ],
        "tracks": [
          "string"
        ],
        "transcript": [
          "string"
        ],
        "video": [
          "string"
        ],
        "vorbis": [
          "string"
        ],
        "wav": [
          "string"
        ],
        "wav24bit": [
          "string"
        ]
      },
      "outputFiles": {
        "aac": {
          "bitrates": [
            "string"
          ],
          "bitrateStrings": [
            "string"
          ],
          "defaultBitrate": "string",
          "displayName": "Ava Chen",
          "endings": [
            "string"
          ],
          "type": "string"
        },
        "alac": {
          "bitrateStrings": [
            "string"
          ],
          "displayName": "Ava Chen",
          "endings": [
            "string"
          ],
          "type": "string"
        },
        "audiogram": {
          "bitrateStrings": [
            "string"
          ],
          "displayName": "Ava Chen",
          "type": "string"
        },
        "chaps": {
          "displayName": "Ava Chen",
          "endings": [
            "string"
          ],
          "type": "string"
        },
        "cutList": {
          "displayName": "Ava Chen",
          "endings": [
            "string"
          ],
          "type": "string"
        },
        "descr": {
          "displayName": "Ava Chen",
          "endings": [
            "string"
          ],
          "type": "string"
        },
        "flac": {
          "bitrateStrings": [
            "string"
          ],
          "displayName": "Ava Chen",
          "endings": [
            "string"
          ],
          "type": "string"
        },
        "image": {
          "displayName": "Ava Chen",
          "type": "string"
        },
        "input": {
          "bitrateStrings": [
            "string"
          ],
          "displayName": "Ava Chen",
          "type": "string"
        },
        "mp3": {
          "bitrates": [
            "string"
          ],
          "bitrateStrings": [
            "string"
          ],
          "defaultBitrate": "string",
          "displayName": "Ava Chen",
          "endings": [
            "string"
          ],
          "type": "string"
        },
        "mp3Vbr": {
          "bitrates": [
            "string"
          ],
          "bitrateStrings": [
            "string"
          ],
          "defaultBitrate": "string",
          "displayName": "Ava Chen",
          "endings": [
            "string"
          ],
          "type": "string"
        },
        "opus": {
          "bitrates": [
            "string"
          ],
          "bitrateStrings": [
            "string"
          ],
          "defaultBitrate": "string",
          "displayName": "Ava Chen",
          "endings": [
            "string"
          ],
          "type": "string"
        },
        "pod2chaps": {
          "displayName": "Ava Chen",
          "endings": [
            "string"
          ],
          "type": "string"
        },
        "psc": {
          "displayName": "Ava Chen",
          "endings": [
            "string"
          ],
          "type": "string"
        },
        "speech": {
          "displayName": "Ava Chen",
          "endings": [
            "string"
          ],
          "type": "string"
        },
        "stats": {
          "displayName": "Ava Chen",
          "endings": [
            "string"
          ],
          "type": "string"
        },
        "subtitle": {
          "displayName": "Ava Chen",
          "endings": [
            "string"
          ],
          "type": "string"
        },
        "tracks": {
          "displayName": "Ava Chen",
          "endings": [
            "string"
          ],
          "type": "string"
        },
        "transcript": {
          "displayName": "Ava Chen",
          "endings": [
            "string"
          ],
          "type": "string"
        },
        "video": {
          "bitrateStrings": [
            "string"
          ],
          "displayName": "Ava Chen",
          "type": "string"
        },
        "vorbis": {
          "bitrates": [
            "string"
          ],
          "bitrateStrings": [
            "string"
          ],
          "defaultBitrate": "string",
          "displayName": "Ava Chen",
          "endings": [
            "string"
          ],
          "type": "string"
        },
        "wav": {
          "bitrateStrings": [
            "string"
          ],
          "displayName": "Ava Chen",
          "endings": [
            "string"
          ],
          "type": "string"
        },
        "wav24bit": {
          "bitrateStrings": [
            "string"
          ],
          "displayName": "Ava Chen",
          "endings": [
            "string"
          ],
          "type": "string"
        }
      },
      "serviceTypes": {
        "acast": {
          "displayName": "Ava Chen",
          "parameters": {
            "show": {
              "defaultValue": "string",
              "displayName": "Ava Chen",
              "type": "string"
            },
            "status": {
              "defaultValue": "string",
              "displayName": "Ava Chen",
              "options": [
                {
                  "displayName": "Ava Chen",
                  "value": "string"
                }
              ],
              "type": "string"
            },
            "type": {
              "defaultValue": "string",
              "displayName": "Ava Chen",
              "options": [
                {
                  "displayName": "Ava Chen",
                  "value": "string"
                }
              ],
              "type": "string"
            }
          }
        },
        "amazons3": {
          "displayName": "Ava Chen",
          "parameters": {}
        },
        "archiveorg": {
          "displayName": "Ava Chen",
          "parameters": {}
        },
        "blubrry": {
          "displayName": "Ava Chen",
          "parameters": {}
        },
        "dropbox": {
          "displayName": "Ava Chen",
          "parameters": {}
        },
        "facebook": {
          "displayName": "Ava Chen",
          "parameters": {
            "embeddable": {
              "defaultValue": true,
              "displayName": "Ava Chen",
              "type": "string"
            },
            "privacy": {
              "defaultValue": "string",
              "displayName": "Ava Chen",
              "options": [
                {
                  "displayName": "Ava Chen",
                  "value": "string"
                }
              ],
              "type": "string"
            }
          }
        },
        "ftp": {
          "displayName": "Ava Chen",
          "parameters": {}
        },
        "gdrive": {
          "displayName": "Ava Chen",
          "parameters": {}
        },
        "generichoster": {
          "captivate": {
            "displayName": "Ava Chen",
            "parameters": {
              "draft": {
                "defaultValue": true,
                "displayName": "Ava Chen",
                "shortName": "Ava Chen",
                "type": "string"
              },
              "type": {
                "defaultValue": "string",
                "displayName": "Ava Chen",
                "options": [
                  {
                    "displayName": "Ava Chen",
                    "value": "string"
                  }
                ],
                "type": "string"
              }
            }
          }
        },
        "letscast": {
          "displayName": "Ava Chen",
          "parameters": {}
        },
        "libsyn": {
          "displayName": "Ava Chen",
          "parameters": {}
        },
        "oauthhoster": {
          "podbean": {
            "displayName": "Ava Chen",
            "parameters": {
              "draft": {
                "defaultValue": true,
                "displayName": "Ava Chen",
                "shortName": "Ava Chen",
                "type": "string"
              },
              "type": {
                "defaultValue": "string",
                "displayName": "Ava Chen",
                "hidden": true,
                "options": [
                  {
                    "displayName": "Ava Chen",
                    "value": "string"
                  }
                ],
                "type": "string"
              }
            }
          }
        },
        "onedrive": {
          "displayName": "Ava Chen",
          "parameters": {}
        },
        "rsscom": {
          "displayName": "Ava Chen",
          "parameters": {
            "podcast": {
              "defaultValue": "string",
              "displayName": "Ava Chen",
              "shortName": "Ava Chen",
              "type": "string"
            }
          }
        },
        "s3storage": {
          "displayName": "Ava Chen",
          "parameters": {}
        },
        "scrybecast": {
          "displayName": "Ava Chen",
          "parameters": {}
        },
        "sftp": {
          "displayName": "Ava Chen",
          "parameters": {}
        },
        "soundcloud": {
          "displayName": "Ava Chen",
          "parameters": {
            "downloadable": {
              "defaultValue": true,
              "displayName": "Ava Chen",
              "type": "string"
            },
            "sharing": {
              "defaultValue": "string",
              "displayName": "Ava Chen",
              "options": [
                {
                  "displayName": "Ava Chen",
                  "value": "string"
                }
              ],
              "type": "string"
            },
            "trackType": {
              "defaultValue": "string",
              "displayName": "Ava Chen",
              "options": [
                {
                  "displayName": "Ava Chen",
                  "value": "string"
                }
              ],
              "type": "string"
            }
          }
        },
        "spreaker": {
          "displayName": "Ava Chen",
          "parameters": {
            "downloadable": {
              "defaultValue": true,
              "displayName": "Ava Chen",
              "type": "string"
            },
            "draft": {
              "defaultValue": true,
              "displayName": "Ava Chen",
              "type": "string"
            },
            "sharing": {
              "defaultValue": "string",
              "displayName": "Ava Chen",
              "options": [
                {
                  "displayName": "Ava Chen",
                  "value": "string"
                }
              ],
              "type": "string"
            },
            "show": {
              "defaultValue": "string",
              "displayName": "Ava Chen",
              "shortName": "Ava Chen",
              "type": "string"
            }
          }
        },
        "webdav": {
          "displayName": "Ava Chen",
          "parameters": {}
        },
        "youtube": {
          "displayName": "Ava Chen",
          "parameters": {
            "category": {
              "defaultValue": "string",
              "displayName": "Ava Chen",
              "options": [
                {
                  "displayName": "Ava Chen",
                  "value": {}
                }
              ],
              "type": "string"
            },
            "privacy": {
              "defaultValue": "string",
              "displayName": "Ava Chen",
              "options": [
                {
                  "displayName": "Ava Chen",
                  "value": "string"
                }
              ],
              "type": "string"
            }
          }
        }
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `algorithms.backforeground.defaultValue` | number |  |
| `algorithms.backforeground.description` | string |  |
| `algorithms.backforeground.displayName` | string |  |
| `algorithms.backforeground.options[].displayName` | number |  |
| `algorithms.backforeground.options[].value` | string |  |
| `algorithms.backforeground.type` | string |  |
| `algorithms.backgroundgain.belongsTo` | string |  |
| `algorithms.backgroundgain.defaultValue` | number |  |
| `algorithms.backgroundgain.displayName` | string |  |
| `algorithms.backgroundgain.options[].displayName` | number |  |
| `algorithms.backgroundgain.options[].value` | number |  |
| `algorithms.backgroundgain.type` | string |  |
| `algorithms.compressor.belongsTo` | string |  |
| `algorithms.compressor.defaultValue` | string |  |
| `algorithms.compressor.displayName` | string |  |
| `algorithms.compressor.options[].displayName` | string |  |
| `algorithms.compressor.options[].value` | string |  |
| `algorithms.compressor.type` | string |  |
| `algorithms.compressorM.belongsTo` | string |  |
| `algorithms.compressorM.defaultValue` | number |  |
| `algorithms.compressorM.displayName` | string |  |
| `algorithms.compressorM.options[].displayName` | string |  |
| `algorithms.compressorM.options[].value` | string |  |
| `algorithms.compressorM.type` | string |  |
| `algorithms.coughCutter.belongsTo` | string |  |
| `algorithms.coughCutter.defaultValue` | boolean |  |
| `algorithms.coughCutter.description` | string |  |
| `algorithms.coughCutter.displayName` | string |  |
| `algorithms.coughCutter.type` | string |  |
| `algorithms.crossgate.defaultValue` | boolean |  |
| `algorithms.crossgate.description` | string |  |
| `algorithms.crossgate.displayName` | string |  |
| `algorithms.crossgate.type` | string |  |
| `algorithms.cutMode.belongsTo` | string |  |
| `algorithms.cutMode.defaultValue` | number |  |
| `algorithms.cutMode.description` | string |  |
| `algorithms.cutMode.displayName` | string |  |
| `algorithms.cutMode.options[].displayName` | string |  |
| `algorithms.cutMode.options[].value` | string |  |
| `algorithms.cutMode.type` | string |  |
| `algorithms.cutter.defaultValue` | boolean |  |
| `algorithms.cutter.description` | string |  |
| `algorithms.cutter.displayName` | string |  |
| `algorithms.cutter.type` | string |  |
| `algorithms.debreathamount.belongsTo` | string |  |
| `algorithms.debreathamount.defaultValue` | number |  |
| `algorithms.debreathamount.displayName` | string |  |
| `algorithms.debreathamount.options[].displayName` | string |  |
| `algorithms.debreathamount.options[].value` | number |  |
| `algorithms.debreathamount.type` | string |  |
| `algorithms.dehum.belongsTo` | string |  |
| `algorithms.dehum.defaultValue` | number |  |
| `algorithms.dehum.displayName` | string |  |
| `algorithms.dehum.options[].displayName` | string |  |
| `algorithms.dehum.options[].value` | number |  |
| `algorithms.dehum.type` | string |  |
| `algorithms.dehumamount.belongsTo` | string |  |
| `algorithms.dehumamount.defaultValue` | number |  |
| `algorithms.dehumamount.displayName` | string |  |
| `algorithms.dehumamount.options[].displayName` | string |  |
| `algorithms.dehumamount.options[].value` | number |  |
| `algorithms.dehumamount.type` | string |  |
| `algorithms.denoise.defaultValue` | boolean |  |
| `algorithms.denoise.description` | string |  |
| `algorithms.denoise.displayName` | string |  |
| `algorithms.denoise.type` | string |  |
| `algorithms.denoiseamount.belongsTo` | string |  |
| `algorithms.denoiseamount.defaultValue` | number |  |
| `algorithms.denoiseamount.displayName` | string |  |
| `algorithms.denoiseamount.options[].displayName` | string |  |
| `algorithms.denoiseamount.options[].value` | number |  |
| `algorithms.denoiseamount.type` | string |  |
| `algorithms.denoisemethod.belongsTo` | string |  |
| `algorithms.denoisemethod.defaultValue` | number |  |
| `algorithms.denoisemethod.displayName` | string |  |
| `algorithms.denoisemethod.options[].displayName` | string |  |
| `algorithms.denoisemethod.options[].value` | string |  |
| `algorithms.denoisemethod.type` | string |  |
| `algorithms.dualmono.belongsTo` | string |  |
| `algorithms.dualmono.defaultValue` | boolean |  |
| `algorithms.dualmono.displayName` | string |  |
| `algorithms.dualmono.type` | string |  |
| `algorithms.duckingFadetime.belongsTo` | string |  |
| `algorithms.duckingFadetime.defaultValue` | number |  |
| `algorithms.duckingFadetime.displayName` | string |  |
| `algorithms.duckingFadetime.options[].displayName` | number |  |
| `algorithms.duckingFadetime.options[].value` | number |  |
| `algorithms.duckingFadetime.type` | string |  |
| `algorithms.fillerCutter.belongsTo` | string |  |
| `algorithms.fillerCutter.defaultValue` | boolean |  |
| `algorithms.fillerCutter.description` | string |  |
| `algorithms.fillerCutter.displayName` | string |  |
| `algorithms.fillerCutter.type` | string |  |
| `algorithms.filtering.defaultValue` | boolean |  |
| `algorithms.filtering.description` | string |  |
| `algorithms.filtering.displayName` | string |  |
| `algorithms.filtering.type` | string |  |
| `algorithms.filtermethod.belongsTo` | string |  |
| `algorithms.filtermethod.defaultValue` | number |  |
| `algorithms.filtermethod.displayName` | string |  |
| `algorithms.filtermethod.options[].displayName` | string |  |
| `algorithms.filtermethod.options[].value` | string |  |
| `algorithms.filtermethod.type` | string |  |
| `algorithms.gain.belongsTo` | string |  |
| `algorithms.gain.defaultValue` | number |  |
| `algorithms.gain.displayName` | string |  |
| `algorithms.gain.options[].displayName` | number |  |
| `algorithms.gain.options[].value` | number |  |
| `algorithms.gain.type` | string |  |
| `algorithms.gate.defaultValue` | boolean |  |
| `algorithms.gate.description` | string |  |
| `algorithms.gate.displayName` | string |  |
| `algorithms.gate.type` | string |  |
| `algorithms.leveler.defaultValue` | boolean |  |
| `algorithms.leveler.description` | string |  |
| `algorithms.leveler.displayName` | string |  |
| `algorithms.leveler.type` | string |  |
| `algorithms.levelerstrength.belongsTo` | string |  |
| `algorithms.levelerstrength.defaultValue` | number |  |
| `algorithms.levelerstrength.displayName` | string |  |
| `algorithms.levelerstrength.options[].displayName` | string |  |
| `algorithms.levelerstrength.options[].value` | number |  |
| `algorithms.levelerstrength.type` | string |  |
| `algorithms.levelerstrengthM.belongsTo` | string |  |
| `algorithms.levelerstrengthM.defaultValue` | number |  |
| `algorithms.levelerstrengthM.displayName` | string |  |
| `algorithms.levelerstrengthM.options[].displayName` | string |  |
| `algorithms.levelerstrengthM.options[].value` | number |  |
| `algorithms.levelerstrengthM.type` | string |  |
| `algorithms.loudnessmethod.belongsTo` | string |  |
| `algorithms.loudnessmethod.defaultValue` | string |  |
| `algorithms.loudnessmethod.displayName` | string |  |
| `algorithms.loudnessmethod.options[].displayName` | string |  |
| `algorithms.loudnessmethod.options[].value` | string |  |
| `algorithms.loudnessmethod.type` | string |  |
| `algorithms.loudnesstarget.belongsTo` | string |  |
| `algorithms.loudnesstarget.defaultValue` | number |  |
| `algorithms.loudnesstarget.displayName` | string |  |
| `algorithms.loudnesstarget.options[].displayName` | string |  |
| `algorithms.loudnesstarget.options[].value` | number |  |
| `algorithms.loudnesstarget.type` | string |  |
| `algorithms.maxlra.belongsTo` | string |  |
| `algorithms.maxlra.defaultValue` | number |  |
| `algorithms.maxlra.displayName` | string |  |
| `algorithms.maxlra.options[].displayName` | string |  |
| `algorithms.maxlra.options[].value` | number |  |
| `algorithms.maxlra.type` | string |  |
| `algorithms.maxm.belongsTo` | string |  |
| `algorithms.maxm.defaultValue` | number |  |
| `algorithms.maxm.displayName` | string |  |
| `algorithms.maxm.options[].displayName` | string |  |
| `algorithms.maxm.options[].value` | number |  |
| `algorithms.maxm.type` | string |  |
| `algorithms.maxpeak.belongsTo` | string |  |
| `algorithms.maxpeak.defaultValue` | number |  |
| `algorithms.maxpeak.displayName` | string |  |
| `algorithms.maxpeak.options[].displayName` | string |  |
| `algorithms.maxpeak.options[].value` | number |  |
| `algorithms.maxpeak.type` | string |  |
| `algorithms.maxs.belongsTo` | string |  |
| `algorithms.maxs.defaultValue` | number |  |
| `algorithms.maxs.displayName` | string |  |
| `algorithms.maxs.options[].displayName` | string |  |
| `algorithms.maxs.options[].value` | number |  |
| `algorithms.maxs.type` | string |  |
| `algorithms.msclassifier.belongsTo` | string |  |
| `algorithms.msclassifier.defaultValue` | number |  |
| `algorithms.msclassifier.displayName` | string |  |
| `algorithms.msclassifier.options[].displayName` | string |  |
| `algorithms.msclassifier.options[].value` | string |  |
| `algorithms.msclassifier.type` | string |  |
| `algorithms.musicCutter.belongsTo` | string |  |
| `algorithms.musicCutter.defaultValue` | boolean |  |
| `algorithms.musicCutter.description` | string |  |
| `algorithms.musicCutter.displayName` | string |  |
| `algorithms.musicCutter.type` | string |  |
| `algorithms.musicgain.belongsTo` | string |  |
| `algorithms.musicgain.defaultValue` | number |  |
| `algorithms.musicgain.displayName` | string |  |
| `algorithms.musicgain.options[].displayName` | string |  |
| `algorithms.musicgain.options[].value` | number |  |
| `algorithms.musicgain.type` | string |  |
| `algorithms.normloudness.defaultValue` | boolean |  |
| `algorithms.normloudness.description` | string |  |
| `algorithms.normloudness.displayName` | string |  |
| `algorithms.normloudness.type` | string |  |
| `algorithms.pan.belongsTo` | string |  |
| `algorithms.pan.defaultValue` | number |  |
| `algorithms.pan.displayName` | string |  |
| `algorithms.pan.options[].displayName` | string |  |
| `algorithms.pan.options[].value` | string |  |
| `algorithms.pan.type` | string |  |
| `algorithms.segments.description` | string |  |
| `algorithms.segments.displayName` | string |  |
| `algorithms.segments.type` | string |  |
| `algorithms.silenceCutter.belongsTo` | string |  |
| `algorithms.silenceCutter.defaultValue` | boolean |  |
| `algorithms.silenceCutter.description` | string |  |
| `algorithms.silenceCutter.displayName` | string |  |
| `algorithms.silenceCutter.type` | string |  |
| `fileEndings.aac[]` | string |  |
| `fileEndings.alac[]` | string |  |
| `fileEndings.audiogram[]` | string |  |
| `fileEndings.chaps[]` | string |  |
| `fileEndings.cutList[]` | string |  |
| `fileEndings.descr[]` | string |  |
| `fileEndings.flac[]` | string |  |
| `fileEndings.image[]` | string |  |
| `fileEndings.input[]` | string |  |
| `fileEndings.mp3[]` | string |  |
| `fileEndings.mp3Vbr[]` | string |  |
| `fileEndings.opus[]` | string |  |
| `fileEndings.pod2chaps[]` | string |  |
| `fileEndings.psc[]` | string |  |
| `fileEndings.speech[]` | string |  |
| `fileEndings.stats[]` | string |  |
| `fileEndings.subtitle[]` | string |  |
| `fileEndings.tracks[]` | string |  |
| `fileEndings.transcript[]` | string |  |
| `fileEndings.video[]` | string |  |
| `fileEndings.vorbis[]` | string |  |
| `fileEndings.wav[]` | string |  |
| `fileEndings.wav24bit[]` | string |  |
| `outputFiles.aac.bitrates[]` | string |  |
| `outputFiles.aac.bitrateStrings[]` | string |  |
| `outputFiles.aac.defaultBitrate` | string |  |
| `outputFiles.aac.displayName` | string |  |
| `outputFiles.aac.endings[]` | string |  |
| `outputFiles.aac.type` | string |  |
| `outputFiles.alac.bitrateStrings[]` | string |  |
| `outputFiles.alac.displayName` | string |  |
| `outputFiles.alac.endings[]` | string |  |
| `outputFiles.alac.type` | string |  |
| `outputFiles.audiogram.bitrateStrings[]` | string |  |
| `outputFiles.audiogram.displayName` | string |  |
| `outputFiles.audiogram.type` | string |  |
| `outputFiles.chaps.displayName` | string |  |
| `outputFiles.chaps.endings[]` | string |  |
| `outputFiles.chaps.type` | string |  |
| `outputFiles.cutList.displayName` | string |  |
| `outputFiles.cutList.endings[]` | string |  |
| `outputFiles.cutList.type` | string |  |
| `outputFiles.descr.displayName` | string |  |
| `outputFiles.descr.endings[]` | string |  |
| `outputFiles.descr.type` | string |  |
| `outputFiles.flac.bitrateStrings[]` | string |  |
| `outputFiles.flac.displayName` | string |  |
| `outputFiles.flac.endings[]` | string |  |
| `outputFiles.flac.type` | string |  |
| `outputFiles.image.displayName` | string |  |
| `outputFiles.image.type` | string |  |
| `outputFiles.input.bitrateStrings[]` | string |  |
| `outputFiles.input.displayName` | string |  |
| `outputFiles.input.type` | string |  |
| `outputFiles.mp3.bitrates[]` | string |  |
| `outputFiles.mp3.bitrateStrings[]` | string |  |
| `outputFiles.mp3.defaultBitrate` | string |  |
| `outputFiles.mp3.displayName` | string |  |
| `outputFiles.mp3.endings[]` | string |  |
| `outputFiles.mp3.type` | string |  |
| `outputFiles.mp3Vbr.bitrates[]` | string |  |
| `outputFiles.mp3Vbr.bitrateStrings[]` | string |  |
| `outputFiles.mp3Vbr.defaultBitrate` | string |  |
| `outputFiles.mp3Vbr.displayName` | string |  |
| `outputFiles.mp3Vbr.endings[]` | string |  |
| `outputFiles.mp3Vbr.type` | string |  |
| `outputFiles.opus.bitrates[]` | string |  |
| `outputFiles.opus.bitrateStrings[]` | string |  |
| `outputFiles.opus.defaultBitrate` | string |  |
| `outputFiles.opus.displayName` | string |  |
| `outputFiles.opus.endings[]` | string |  |
| `outputFiles.opus.type` | string |  |
| `outputFiles.pod2chaps.displayName` | string |  |
| `outputFiles.pod2chaps.endings[]` | string |  |
| `outputFiles.pod2chaps.type` | string |  |
| `outputFiles.psc.displayName` | string |  |
| `outputFiles.psc.endings[]` | string |  |
| `outputFiles.psc.type` | string |  |
| `outputFiles.speech.displayName` | string |  |
| `outputFiles.speech.endings[]` | string |  |
| `outputFiles.speech.type` | string |  |
| `outputFiles.stats.displayName` | string |  |
| `outputFiles.stats.endings[]` | string |  |
| `outputFiles.stats.type` | string |  |
| `outputFiles.subtitle.displayName` | string |  |
| `outputFiles.subtitle.endings[]` | string |  |
| `outputFiles.subtitle.type` | string |  |
| `outputFiles.tracks.displayName` | string |  |
| `outputFiles.tracks.endings[]` | string |  |
| `outputFiles.tracks.type` | string |  |
| `outputFiles.transcript.displayName` | string |  |
| `outputFiles.transcript.endings[]` | string |  |
| `outputFiles.transcript.type` | string |  |
| `outputFiles.video.bitrateStrings[]` | string |  |
| `outputFiles.video.displayName` | string |  |
| `outputFiles.video.type` | string |  |
| `outputFiles.vorbis.bitrates[]` | string |  |
| `outputFiles.vorbis.bitrateStrings[]` | string |  |
| `outputFiles.vorbis.defaultBitrate` | string |  |
| `outputFiles.vorbis.displayName` | string |  |
| `outputFiles.vorbis.endings[]` | string |  |
| `outputFiles.vorbis.type` | string |  |
| `outputFiles.wav.bitrateStrings[]` | string |  |
| `outputFiles.wav.displayName` | string |  |
| `outputFiles.wav.endings[]` | string |  |
| `outputFiles.wav.type` | string |  |
| `outputFiles.wav24bit.bitrateStrings[]` | string |  |
| `outputFiles.wav24bit.displayName` | string |  |
| `outputFiles.wav24bit.endings[]` | string |  |
| `outputFiles.wav24bit.type` | string |  |
| `serviceTypes.acast.displayName` | string |  |
| `serviceTypes.acast.parameters.show.defaultValue` | string |  |
| `serviceTypes.acast.parameters.show.displayName` | string |  |
| `serviceTypes.acast.parameters.show.type` | string |  |
| `serviceTypes.acast.parameters.status.defaultValue` | string |  |
| `serviceTypes.acast.parameters.status.displayName` | string |  |
| `serviceTypes.acast.parameters.status.options[].displayName` | string |  |
| `serviceTypes.acast.parameters.status.options[].value` | string |  |
| `serviceTypes.acast.parameters.status.type` | string |  |
| `serviceTypes.acast.parameters.type.defaultValue` | string |  |
| `serviceTypes.acast.parameters.type.displayName` | string |  |
| `serviceTypes.acast.parameters.type.options[].displayName` | string |  |
| `serviceTypes.acast.parameters.type.options[].value` | string |  |
| `serviceTypes.acast.parameters.type.type` | string |  |
| `serviceTypes.amazons3.displayName` | string |  |
| `serviceTypes.amazons3.parameters` | object |  |
| `serviceTypes.archiveorg.displayName` | string |  |
| `serviceTypes.archiveorg.parameters` | object |  |
| `serviceTypes.blubrry.displayName` | string |  |
| `serviceTypes.blubrry.parameters` | object |  |
| `serviceTypes.dropbox.displayName` | string |  |
| `serviceTypes.dropbox.parameters` | object |  |
| `serviceTypes.facebook.displayName` | string |  |
| `serviceTypes.facebook.parameters.embeddable.defaultValue` | boolean |  |
| `serviceTypes.facebook.parameters.embeddable.displayName` | string |  |
| `serviceTypes.facebook.parameters.embeddable.type` | string |  |
| `serviceTypes.facebook.parameters.privacy.defaultValue` | string |  |
| `serviceTypes.facebook.parameters.privacy.displayName` | string |  |
| `serviceTypes.facebook.parameters.privacy.options[].displayName` | string |  |
| `serviceTypes.facebook.parameters.privacy.options[].value` | string |  |
| `serviceTypes.facebook.parameters.privacy.type` | string |  |
| `serviceTypes.ftp.displayName` | string |  |
| `serviceTypes.ftp.parameters` | object |  |
| `serviceTypes.gdrive.displayName` | string |  |
| `serviceTypes.gdrive.parameters` | object |  |
| `serviceTypes.generichoster.captivate.displayName` | string |  |
| `serviceTypes.generichoster.captivate.parameters.draft.defaultValue` | boolean |  |
| `serviceTypes.generichoster.captivate.parameters.draft.displayName` | string |  |
| `serviceTypes.generichoster.captivate.parameters.draft.shortName` | string |  |
| `serviceTypes.generichoster.captivate.parameters.draft.type` | string |  |
| `serviceTypes.generichoster.captivate.parameters.type.defaultValue` | string |  |
| `serviceTypes.generichoster.captivate.parameters.type.displayName` | string |  |
| `serviceTypes.generichoster.captivate.parameters.type.options[].displayName` | string |  |
| `serviceTypes.generichoster.captivate.parameters.type.options[].value` | string |  |
| `serviceTypes.generichoster.captivate.parameters.type.type` | string |  |
| `serviceTypes.letscast.displayName` | string |  |
| `serviceTypes.letscast.parameters` | object |  |
| `serviceTypes.libsyn.displayName` | string |  |
| `serviceTypes.libsyn.parameters` | object |  |
| `serviceTypes.oauthhoster.podbean.displayName` | string |  |
| `serviceTypes.oauthhoster.podbean.parameters.draft.defaultValue` | boolean |  |
| `serviceTypes.oauthhoster.podbean.parameters.draft.displayName` | string |  |
| `serviceTypes.oauthhoster.podbean.parameters.draft.shortName` | string |  |
| `serviceTypes.oauthhoster.podbean.parameters.draft.type` | string |  |
| `serviceTypes.oauthhoster.podbean.parameters.type.defaultValue` | string |  |
| `serviceTypes.oauthhoster.podbean.parameters.type.displayName` | string |  |
| `serviceTypes.oauthhoster.podbean.parameters.type.hidden` | boolean |  |
| `serviceTypes.oauthhoster.podbean.parameters.type.options[].displayName` | string |  |
| `serviceTypes.oauthhoster.podbean.parameters.type.options[].value` | string |  |
| `serviceTypes.oauthhoster.podbean.parameters.type.type` | string |  |
| `serviceTypes.onedrive.displayName` | string |  |
| `serviceTypes.onedrive.parameters` | object |  |
| `serviceTypes.rsscom.displayName` | string |  |
| `serviceTypes.rsscom.parameters.podcast.defaultValue` | string |  |
| `serviceTypes.rsscom.parameters.podcast.displayName` | string |  |
| `serviceTypes.rsscom.parameters.podcast.shortName` | string |  |
| `serviceTypes.rsscom.parameters.podcast.type` | string |  |
| `serviceTypes.s3storage.displayName` | string |  |
| `serviceTypes.s3storage.parameters` | object |  |
| `serviceTypes.scrybecast.displayName` | string |  |
| `serviceTypes.scrybecast.parameters` | object |  |
| `serviceTypes.sftp.displayName` | string |  |
| `serviceTypes.sftp.parameters` | object |  |
| `serviceTypes.soundcloud.displayName` | string |  |
| `serviceTypes.soundcloud.parameters.downloadable.defaultValue` | boolean |  |
| `serviceTypes.soundcloud.parameters.downloadable.displayName` | string |  |
| `serviceTypes.soundcloud.parameters.downloadable.type` | string |  |
| `serviceTypes.soundcloud.parameters.sharing.defaultValue` | string |  |
| `serviceTypes.soundcloud.parameters.sharing.displayName` | string |  |
| `serviceTypes.soundcloud.parameters.sharing.options[].displayName` | string |  |
| `serviceTypes.soundcloud.parameters.sharing.options[].value` | string |  |
| `serviceTypes.soundcloud.parameters.sharing.type` | string |  |
| `serviceTypes.soundcloud.parameters.trackType.defaultValue` | string |  |
| `serviceTypes.soundcloud.parameters.trackType.displayName` | string |  |
| `serviceTypes.soundcloud.parameters.trackType.options[].displayName` | string |  |
| `serviceTypes.soundcloud.parameters.trackType.options[].value` | string |  |
| `serviceTypes.soundcloud.parameters.trackType.type` | string |  |
| `serviceTypes.spreaker.displayName` | string |  |
| `serviceTypes.spreaker.parameters.downloadable.defaultValue` | boolean |  |
| `serviceTypes.spreaker.parameters.downloadable.displayName` | string |  |
| `serviceTypes.spreaker.parameters.downloadable.type` | string |  |
| `serviceTypes.spreaker.parameters.draft.defaultValue` | boolean |  |
| `serviceTypes.spreaker.parameters.draft.displayName` | string |  |
| `serviceTypes.spreaker.parameters.draft.type` | string |  |
| `serviceTypes.spreaker.parameters.sharing.defaultValue` | string |  |
| `serviceTypes.spreaker.parameters.sharing.displayName` | string |  |
| `serviceTypes.spreaker.parameters.sharing.options[].displayName` | string |  |
| `serviceTypes.spreaker.parameters.sharing.options[].value` | string |  |
| `serviceTypes.spreaker.parameters.sharing.type` | string |  |
| `serviceTypes.spreaker.parameters.show.defaultValue` | string |  |
| `serviceTypes.spreaker.parameters.show.displayName` | string |  |
| `serviceTypes.spreaker.parameters.show.shortName` | string |  |
| `serviceTypes.spreaker.parameters.show.type` | string |  |
| `serviceTypes.webdav.displayName` | string |  |
| `serviceTypes.webdav.parameters` | object |  |
| `serviceTypes.youtube.displayName` | string |  |
| `serviceTypes.youtube.parameters.category.defaultValue` | string |  |
| `serviceTypes.youtube.parameters.category.displayName` | string |  |
| `serviceTypes.youtube.parameters.category.options[].displayName` | string |  |
| `serviceTypes.youtube.parameters.category.options[].value` | object |  |
| `serviceTypes.youtube.parameters.category.type` | string |  |
| `serviceTypes.youtube.parameters.privacy.defaultValue` | string |  |
| `serviceTypes.youtube.parameters.privacy.displayName` | string |  |
| `serviceTypes.youtube.parameters.privacy.options[].displayName` | string |  |
| `serviceTypes.youtube.parameters.privacy.options[].value` | string |  |
| `serviceTypes.youtube.parameters.privacy.type` | string |  |

## Native endpoint

Through the native Auphonic API, this operation is `GET /info.json` (base URL `https://auphonic.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-api-information.md) for the provider-specific parameters and requirements.

