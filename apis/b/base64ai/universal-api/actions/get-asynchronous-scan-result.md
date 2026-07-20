# Base64.ai: Get Asynchronous Scan Result

Retrieves an asynchronous scan result from Base64.ai.

```
GET https://connect.mindcloud.co/v1/universal/base64ai/latest/actions/get-asynchronous-scan-result
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Base64.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/base64ai/latest/actions/get-asynchronous-scan-result?connectionId=$CONNECTION_ID&asyncFileUUID=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "asyncFileUUID": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/base64ai/latest/actions/get-asynchronous-scan-result?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `asyncFileUUID` | string | yes | Asynchronous scan identifier returned by Base64.ai. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "features": {
        "barcodes": {
          "mrz": [
            "string"
          ]
        },
        "creditsSpent": 1,
        "dom": {
          "box": {
            "bottom": 1,
            "height": 1,
            "left": 1,
            "pageNumber": {},
            "right": 1,
            "top": 1,
            "width": 1
          },
          "confidence": 1,
          "pages": [
            {
              "blocks": [
                {
                  "box": {
                    "bottom": 1,
                    "height": 1,
                    "left": 1,
                    "pageNumber": 1,
                    "right": 1,
                    "top": 1,
                    "width": 1
                  },
                  "confidence": 1,
                  "lines": [
                    {
                      "box": {
                        "bottom": 1,
                        "height": 1,
                        "left": 1,
                        "pageNumber": 1,
                        "right": 1,
                        "top": 1,
                        "width": 1
                      },
                      "confidence": 1,
                      "location": {
                        "bottomLeft": {
                          "x": 1,
                          "y": 1
                        },
                        "bottomRight": {
                          "x": 1,
                          "y": 1
                        },
                        "pageNumber": 1,
                        "topLeft": {
                          "x": 1,
                          "y": 1
                        },
                        "topRight": {
                          "x": 1,
                          "y": 1
                        }
                      },
                      "text": "string",
                      "words": [
                        {
                          "box": {
                            "bottom": 1,
                            "height": 1,
                            "left": 1,
                            "pageNumber": 1,
                            "right": 1,
                            "top": 1,
                            "width": 1
                          },
                          "confidence": 1,
                          "location": {
                            "bottomLeft": {
                              "x": 1,
                              "y": 1
                            },
                            "bottomRight": {
                              "x": 1,
                              "y": 1
                            },
                            "pageNumber": 1,
                            "topLeft": {
                              "x": 1,
                              "y": 1
                            },
                            "topRight": {
                              "x": 1,
                              "y": 1
                            }
                          },
                          "text": "string"
                        }
                      ]
                    }
                  ],
                  "location": {
                    "bottomLeft": {
                      "x": 1,
                      "y": 1
                    },
                    "bottomRight": {
                      "x": 1,
                      "y": 1
                    },
                    "pageNumber": 1,
                    "topLeft": {
                      "x": 1,
                      "y": 1
                    },
                    "topRight": {
                      "x": 1,
                      "y": 1
                    }
                  },
                  "text": "string"
                }
              ],
              "box": {
                "bottom": 1,
                "height": 1,
                "left": 1,
                "pageNumber": 1,
                "right": 1,
                "top": 1,
                "width": 1
              },
              "confidence": 1,
              "location": {
                "bottomLeft": {
                  "x": 1,
                  "y": 1
                },
                "bottomRight": {
                  "x": 1,
                  "y": 1
                },
                "pageNumber": 1,
                "topLeft": {
                  "x": 1,
                  "y": 1
                },
                "topRight": {
                  "x": 1,
                  "y": 1
                }
              },
              "properties": {
                "dpiX": 1,
                "dpiY": 1,
                "height": 1,
                "mimeType": "string",
                "normalizedHeight": 1,
                "normalizedWidth": 1,
                "rotationAngle": 1,
                "width": 1
              },
              "text": "string"
            }
          ],
          "text": "string"
        },
        "faces": [
          {
            "bottom": 1,
            "bottomLeft": {
              "x": 1,
              "y": 1
            },
            "bottomRight": {
              "x": 1,
              "y": 1
            },
            "confidence": 1,
            "height": 1,
            "image": "string",
            "left": 1,
            "pageNumber": 1,
            "right": 1,
            "top": 1,
            "topLeft": {
              "x": 1,
              "y": 1
            },
            "topRight": {
              "x": 1,
              "y": 1
            },
            "width": 1
          }
        ],
        "fraud": {
          "indicators": [
            {
              "category": "string",
              "confidence": "string",
              "description": "string",
              "evidences": [
                {
                  "ocr": "string"
                }
              ],
              "name": "Ava Chen",
              "risk": "string"
            }
          ],
          "risk": "string"
        },
        "properties": {
          "createdAt": "2026-05-07T12:00:00.000Z",
          "documentPageCount": 1,
          "dpiX": 1,
          "dpiY": 1,
          "flowID": "string",
          "height": 1,
          "isEditable": true,
          "isGlareFree": true,
          "isInFocus": true,
          "isSelectable": true,
          "mimeType": "string",
          "originalFileName": "Ava Chen",
          "pageCount": 1,
          "rotationAngle": 1,
          "startPage": 1,
          "width": 1
        },
        "signatures": [
          {
            "bottom": 1,
            "bottomLeft": {
              "x": 1,
              "y": 1
            },
            "bottomRight": {
              "x": 1,
              "y": 1
            },
            "confidence": 1,
            "height": 1,
            "image": "string",
            "left": 1,
            "pageNumber": 1,
            "right": 1,
            "top": 1,
            "topLeft": {
              "x": 1,
              "y": 1
            },
            "topRight": {
              "x": 1,
              "y": 1
            },
            "width": 1
          }
        ]
      },
      "fields": {
        "age": {
          "confidence": 1,
          "isValid": true,
          "key": "string",
          "location": {
            "bottomLeft": {
              "x": 1,
              "y": 1
            },
            "bottomRight": {
              "x": 1,
              "y": 1
            },
            "pageNumber": 1,
            "topLeft": {
              "x": 1,
              "y": 1
            },
            "topRight": {
              "x": 1,
              "y": 1
            }
          },
          "ocrText": "string",
          "type": "string",
          "value": 1
        },
        "countryCode": {
          "confidence": 1,
          "isValid": true,
          "key": "string",
          "type": "string",
          "value": "string"
        },
        "countryName": {
          "confidence": 1,
          "isValid": true,
          "key": "Ava Chen",
          "type": "Ava Chen",
          "value": "Ava Chen"
        },
        "dateOfBirth": {
          "confidence": 1,
          "isValid": true,
          "key": "string",
          "location": {
            "bottomLeft": {
              "x": 1,
              "y": 1
            },
            "bottomRight": {
              "x": 1,
              "y": 1
            },
            "pageNumber": 1,
            "topLeft": {
              "x": 1,
              "y": 1
            },
            "topRight": {
              "x": 1,
              "y": 1
            }
          },
          "ocrText": "string",
          "type": "string",
          "value": "string"
        },
        "documentNumber": {
          "confidence": 1,
          "key": "string",
          "location": {
            "bottomLeft": {
              "x": 1,
              "y": 1
            },
            "bottomRight": {
              "x": 1,
              "y": 1
            },
            "pageNumber": 1,
            "topLeft": {
              "x": 1,
              "y": 1
            },
            "topRight": {
              "x": 1,
              "y": 1
            }
          },
          "value": "string"
        },
        "documentType": {
          "confidence": 1,
          "isValid": true,
          "key": "string",
          "type": "string",
          "value": "string"
        },
        "expirationDate": {
          "confidence": 1,
          "isValid": true,
          "key": "string",
          "location": {
            "bottomLeft": {
              "x": 1,
              "y": 1
            },
            "bottomRight": {
              "x": 1,
              "y": 1
            },
            "pageNumber": 1,
            "topLeft": {
              "x": 1,
              "y": 1
            },
            "topRight": {
              "x": 1,
              "y": 1
            }
          },
          "ocrText": "string",
          "type": "string",
          "value": "string"
        },
        "familyName": {
          "confidence": 1,
          "key": "Ava Chen",
          "location": {
            "bottomLeft": {
              "x": 1,
              "y": 1
            },
            "bottomRight": {
              "x": 1,
              "y": 1
            },
            "pageNumber": 1,
            "topLeft": {
              "x": 1,
              "y": 1
            },
            "topRight": {
              "x": 1,
              "y": 1
            }
          },
          "value": "Ava Chen"
        },
        "familyNameLocal": {
          "confidence": 1,
          "key": "Ava Chen",
          "location": {
            "bottomLeft": {
              "x": 1,
              "y": 1
            },
            "bottomRight": {
              "x": 1,
              "y": 1
            },
            "pageNumber": 1,
            "topLeft": {
              "x": 1,
              "y": 1
            },
            "topRight": {
              "x": 1,
              "y": 1
            }
          },
          "value": "Ava Chen"
        },
        "givenName": {
          "confidence": 1,
          "key": "Ava Chen",
          "location": {
            "bottomLeft": {
              "x": 1,
              "y": 1
            },
            "bottomRight": {
              "x": 1,
              "y": 1
            },
            "pageNumber": 1,
            "topLeft": {
              "x": 1,
              "y": 1
            },
            "topRight": {
              "x": 1,
              "y": 1
            }
          },
          "value": "Ava Chen"
        },
        "givenNameLocal": {
          "confidence": 1,
          "key": "Ava Chen",
          "location": {
            "bottomLeft": {
              "x": 1,
              "y": 1
            },
            "bottomRight": {
              "x": 1,
              "y": 1
            },
            "pageNumber": 1,
            "topLeft": {
              "x": 1,
              "y": 1
            },
            "topRight": {
              "x": 1,
              "y": 1
            }
          },
          "value": "Ava Chen"
        },
        "issueDate": {
          "confidence": 1,
          "isValid": true,
          "key": "string",
          "location": {
            "bottomLeft": {
              "x": 1,
              "y": 1
            },
            "bottomRight": {
              "x": 1,
              "y": 1
            },
            "pageNumber": 1,
            "topLeft": {
              "x": 1,
              "y": 1
            },
            "topRight": {
              "x": 1,
              "y": 1
            }
          },
          "ocrText": "string",
          "value": "string"
        },
        "issuingState": {
          "confidence": 1,
          "key": "string",
          "location": {
            "bottomLeft": {
              "x": 1,
              "y": 1
            },
            "bottomRight": {
              "x": 1,
              "y": 1
            },
            "pageNumber": 1,
            "topLeft": {
              "x": 1,
              "y": 1
            },
            "topRight": {
              "x": 1,
              "y": 1
            }
          },
          "value": "string"
        },
        "nationality": {
          "confidence": 1,
          "key": "string",
          "location": {
            "bottomLeft": {
              "x": 1,
              "y": 1
            },
            "bottomRight": {
              "x": 1,
              "y": 1
            },
            "pageNumber": 1,
            "topLeft": {
              "x": 1,
              "y": 1
            },
            "topRight": {
              "x": 1,
              "y": 1
            }
          },
          "value": "string"
        },
        "personalNumber": {
          "confidence": 1,
          "key": "string",
          "location": {
            "bottomLeft": {
              "x": 1,
              "y": 1
            },
            "bottomRight": {
              "x": 1,
              "y": 1
            },
            "pageNumber": 1,
            "topLeft": {
              "x": 1,
              "y": 1
            },
            "topRight": {
              "x": 1,
              "y": 1
            }
          },
          "value": "string"
        },
        "placeOfBirth": {
          "confidence": 1,
          "key": "string",
          "location": {
            "bottomLeft": {
              "x": 1,
              "y": 1
            },
            "bottomRight": {
              "x": 1,
              "y": 1
            },
            "pageNumber": 1,
            "topLeft": {
              "x": 1,
              "y": 1
            },
            "topRight": {
              "x": 1,
              "y": 1
            }
          },
          "value": "string"
        },
        "sex": {
          "confidence": 1,
          "key": "string",
          "location": {
            "bottomLeft": {
              "x": 1,
              "y": 1
            },
            "bottomRight": {
              "x": 1,
              "y": 1
            },
            "pageNumber": 1,
            "topLeft": {
              "x": 1,
              "y": 1
            },
            "topRight": {
              "x": 1,
              "y": 1
            }
          },
          "value": "string"
        }
      },
      "model": {
        "confidence": 1,
        "isValid": true,
        "name": "Ava Chen",
        "shape": "string",
        "type": "string"
      },
      "ocr": "string",
      "status": "string",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `features.barcodes.mrz[]` | string |  |
| `features.creditsSpent` | number |  |
| `features.dom.box.bottom` | number |  |
| `features.dom.box.height` | number |  |
| `features.dom.box.left` | number |  |
| `features.dom.box.pageNumber` | object |  |
| `features.dom.box.right` | number |  |
| `features.dom.box.top` | number |  |
| `features.dom.box.width` | number |  |
| `features.dom.confidence` | number |  |
| `features.dom.pages[].blocks[].box.bottom` | number |  |
| `features.dom.pages[].blocks[].box.height` | number |  |
| `features.dom.pages[].blocks[].box.left` | number |  |
| `features.dom.pages[].blocks[].box.pageNumber` | number |  |
| `features.dom.pages[].blocks[].box.right` | number |  |
| `features.dom.pages[].blocks[].box.top` | number |  |
| `features.dom.pages[].blocks[].box.width` | number |  |
| `features.dom.pages[].blocks[].confidence` | number |  |
| `features.dom.pages[].blocks[].lines[].box.bottom` | number |  |
| `features.dom.pages[].blocks[].lines[].box.height` | number |  |
| `features.dom.pages[].blocks[].lines[].box.left` | number |  |
| `features.dom.pages[].blocks[].lines[].box.pageNumber` | number |  |
| `features.dom.pages[].blocks[].lines[].box.right` | number |  |
| `features.dom.pages[].blocks[].lines[].box.top` | number |  |
| `features.dom.pages[].blocks[].lines[].box.width` | number |  |
| `features.dom.pages[].blocks[].lines[].confidence` | number |  |
| `features.dom.pages[].blocks[].lines[].location.bottomLeft.x` | number |  |
| `features.dom.pages[].blocks[].lines[].location.bottomLeft.y` | number |  |
| `features.dom.pages[].blocks[].lines[].location.bottomRight.x` | number |  |
| `features.dom.pages[].blocks[].lines[].location.bottomRight.y` | number |  |
| `features.dom.pages[].blocks[].lines[].location.pageNumber` | number |  |
| `features.dom.pages[].blocks[].lines[].location.topLeft.x` | number |  |
| `features.dom.pages[].blocks[].lines[].location.topLeft.y` | number |  |
| `features.dom.pages[].blocks[].lines[].location.topRight.x` | number |  |
| `features.dom.pages[].blocks[].lines[].location.topRight.y` | number |  |
| `features.dom.pages[].blocks[].lines[].text` | string |  |
| `features.dom.pages[].blocks[].lines[].words[].box.bottom` | number |  |
| `features.dom.pages[].blocks[].lines[].words[].box.height` | number |  |
| `features.dom.pages[].blocks[].lines[].words[].box.left` | number |  |
| `features.dom.pages[].blocks[].lines[].words[].box.pageNumber` | number |  |
| `features.dom.pages[].blocks[].lines[].words[].box.right` | number |  |
| `features.dom.pages[].blocks[].lines[].words[].box.top` | number |  |
| `features.dom.pages[].blocks[].lines[].words[].box.width` | number |  |
| `features.dom.pages[].blocks[].lines[].words[].confidence` | number |  |
| `features.dom.pages[].blocks[].lines[].words[].location.bottomLeft.x` | number |  |
| `features.dom.pages[].blocks[].lines[].words[].location.bottomLeft.y` | number |  |
| `features.dom.pages[].blocks[].lines[].words[].location.bottomRight.x` | number |  |
| `features.dom.pages[].blocks[].lines[].words[].location.bottomRight.y` | number |  |
| `features.dom.pages[].blocks[].lines[].words[].location.pageNumber` | number |  |
| `features.dom.pages[].blocks[].lines[].words[].location.topLeft.x` | number |  |
| `features.dom.pages[].blocks[].lines[].words[].location.topLeft.y` | number |  |
| `features.dom.pages[].blocks[].lines[].words[].location.topRight.x` | number |  |
| `features.dom.pages[].blocks[].lines[].words[].location.topRight.y` | number |  |
| `features.dom.pages[].blocks[].lines[].words[].text` | string |  |
| `features.dom.pages[].blocks[].location.bottomLeft.x` | number |  |
| `features.dom.pages[].blocks[].location.bottomLeft.y` | number |  |
| `features.dom.pages[].blocks[].location.bottomRight.x` | number |  |
| `features.dom.pages[].blocks[].location.bottomRight.y` | number |  |
| `features.dom.pages[].blocks[].location.pageNumber` | number |  |
| `features.dom.pages[].blocks[].location.topLeft.x` | number |  |
| `features.dom.pages[].blocks[].location.topLeft.y` | number |  |
| `features.dom.pages[].blocks[].location.topRight.x` | number |  |
| `features.dom.pages[].blocks[].location.topRight.y` | number |  |
| `features.dom.pages[].blocks[].text` | string |  |
| `features.dom.pages[].box.bottom` | number |  |
| `features.dom.pages[].box.height` | number |  |
| `features.dom.pages[].box.left` | number |  |
| `features.dom.pages[].box.pageNumber` | number |  |
| `features.dom.pages[].box.right` | number |  |
| `features.dom.pages[].box.top` | number |  |
| `features.dom.pages[].box.width` | number |  |
| `features.dom.pages[].confidence` | number |  |
| `features.dom.pages[].location.bottomLeft.x` | number |  |
| `features.dom.pages[].location.bottomLeft.y` | number |  |
| `features.dom.pages[].location.bottomRight.x` | number |  |
| `features.dom.pages[].location.bottomRight.y` | number |  |
| `features.dom.pages[].location.pageNumber` | number |  |
| `features.dom.pages[].location.topLeft.x` | number |  |
| `features.dom.pages[].location.topLeft.y` | number |  |
| `features.dom.pages[].location.topRight.x` | number |  |
| `features.dom.pages[].location.topRight.y` | number |  |
| `features.dom.pages[].properties.dpiX` | number |  |
| `features.dom.pages[].properties.dpiY` | number |  |
| `features.dom.pages[].properties.height` | number |  |
| `features.dom.pages[].properties.mimeType` | string |  |
| `features.dom.pages[].properties.normalizedHeight` | number |  |
| `features.dom.pages[].properties.normalizedWidth` | number |  |
| `features.dom.pages[].properties.rotationAngle` | number |  |
| `features.dom.pages[].properties.width` | number |  |
| `features.dom.pages[].text` | string |  |
| `features.dom.text` | string |  |
| `features.faces[].bottom` | number |  |
| `features.faces[].bottomLeft.x` | number |  |
| `features.faces[].bottomLeft.y` | number |  |
| `features.faces[].bottomRight.x` | number |  |
| `features.faces[].bottomRight.y` | number |  |
| `features.faces[].confidence` | number |  |
| `features.faces[].height` | number |  |
| `features.faces[].image` | string |  |
| `features.faces[].left` | number |  |
| `features.faces[].pageNumber` | number |  |
| `features.faces[].right` | number |  |
| `features.faces[].top` | number |  |
| `features.faces[].topLeft.x` | number |  |
| `features.faces[].topLeft.y` | number |  |
| `features.faces[].topRight.x` | number |  |
| `features.faces[].topRight.y` | number |  |
| `features.faces[].width` | number |  |
| `features.fraud.indicators[].category` | string |  |
| `features.fraud.indicators[].confidence` | string |  |
| `features.fraud.indicators[].description` | string |  |
| `features.fraud.indicators[].evidences[].ocr` | string |  |
| `features.fraud.indicators[].name` | string |  |
| `features.fraud.indicators[].risk` | string |  |
| `features.fraud.risk` | string |  |
| `features.properties.createdAt` | date |  |
| `features.properties.documentPageCount` | number |  |
| `features.properties.dpiX` | number |  |
| `features.properties.dpiY` | number |  |
| `features.properties.flowID` | string |  |
| `features.properties.height` | number |  |
| `features.properties.isEditable` | boolean |  |
| `features.properties.isGlareFree` | boolean |  |
| `features.properties.isInFocus` | boolean |  |
| `features.properties.isSelectable` | boolean |  |
| `features.properties.mimeType` | string |  |
| `features.properties.originalFileName` | string |  |
| `features.properties.pageCount` | number |  |
| `features.properties.rotationAngle` | number |  |
| `features.properties.startPage` | number |  |
| `features.properties.width` | number |  |
| `features.signatures[].bottom` | number |  |
| `features.signatures[].bottomLeft.x` | number |  |
| `features.signatures[].bottomLeft.y` | number |  |
| `features.signatures[].bottomRight.x` | number |  |
| `features.signatures[].bottomRight.y` | number |  |
| `features.signatures[].confidence` | number |  |
| `features.signatures[].height` | number |  |
| `features.signatures[].image` | string |  |
| `features.signatures[].left` | number |  |
| `features.signatures[].pageNumber` | number |  |
| `features.signatures[].right` | number |  |
| `features.signatures[].top` | number |  |
| `features.signatures[].topLeft.x` | number |  |
| `features.signatures[].topLeft.y` | number |  |
| `features.signatures[].topRight.x` | number |  |
| `features.signatures[].topRight.y` | number |  |
| `features.signatures[].width` | number |  |
| `fields.age.confidence` | number |  |
| `fields.age.isValid` | boolean |  |
| `fields.age.key` | string |  |
| `fields.age.location.bottomLeft.x` | number |  |
| `fields.age.location.bottomLeft.y` | number |  |
| `fields.age.location.bottomRight.x` | number |  |
| `fields.age.location.bottomRight.y` | number |  |
| `fields.age.location.pageNumber` | number |  |
| `fields.age.location.topLeft.x` | number |  |
| `fields.age.location.topLeft.y` | number |  |
| `fields.age.location.topRight.x` | number |  |
| `fields.age.location.topRight.y` | number |  |
| `fields.age.ocrText` | string |  |
| `fields.age.type` | string |  |
| `fields.age.value` | number |  |
| `fields.countryCode.confidence` | number |  |
| `fields.countryCode.isValid` | boolean |  |
| `fields.countryCode.key` | string |  |
| `fields.countryCode.type` | string |  |
| `fields.countryCode.value` | string |  |
| `fields.countryName.confidence` | number |  |
| `fields.countryName.isValid` | boolean |  |
| `fields.countryName.key` | string |  |
| `fields.countryName.type` | string |  |
| `fields.countryName.value` | string |  |
| `fields.dateOfBirth.confidence` | number |  |
| `fields.dateOfBirth.isValid` | boolean |  |
| `fields.dateOfBirth.key` | string |  |
| `fields.dateOfBirth.location.bottomLeft.x` | number |  |
| `fields.dateOfBirth.location.bottomLeft.y` | number |  |
| `fields.dateOfBirth.location.bottomRight.x` | number |  |
| `fields.dateOfBirth.location.bottomRight.y` | number |  |
| `fields.dateOfBirth.location.pageNumber` | number |  |
| `fields.dateOfBirth.location.topLeft.x` | number |  |
| `fields.dateOfBirth.location.topLeft.y` | number |  |
| `fields.dateOfBirth.location.topRight.x` | number |  |
| `fields.dateOfBirth.location.topRight.y` | number |  |
| `fields.dateOfBirth.ocrText` | string |  |
| `fields.dateOfBirth.type` | string |  |
| `fields.dateOfBirth.value` | string |  |
| `fields.documentNumber.confidence` | number |  |
| `fields.documentNumber.key` | string |  |
| `fields.documentNumber.location.bottomLeft.x` | number |  |
| `fields.documentNumber.location.bottomLeft.y` | number |  |
| `fields.documentNumber.location.bottomRight.x` | number |  |
| `fields.documentNumber.location.bottomRight.y` | number |  |
| `fields.documentNumber.location.pageNumber` | number |  |
| `fields.documentNumber.location.topLeft.x` | number |  |
| `fields.documentNumber.location.topLeft.y` | number |  |
| `fields.documentNumber.location.topRight.x` | number |  |
| `fields.documentNumber.location.topRight.y` | number |  |
| `fields.documentNumber.value` | string |  |
| `fields.documentType.confidence` | number |  |
| `fields.documentType.isValid` | boolean |  |
| `fields.documentType.key` | string |  |
| `fields.documentType.type` | string |  |
| `fields.documentType.value` | string |  |
| `fields.expirationDate.confidence` | number |  |
| `fields.expirationDate.isValid` | boolean |  |
| `fields.expirationDate.key` | string |  |
| `fields.expirationDate.location.bottomLeft.x` | number |  |
| `fields.expirationDate.location.bottomLeft.y` | number |  |
| `fields.expirationDate.location.bottomRight.x` | number |  |
| `fields.expirationDate.location.bottomRight.y` | number |  |
| `fields.expirationDate.location.pageNumber` | number |  |
| `fields.expirationDate.location.topLeft.x` | number |  |
| `fields.expirationDate.location.topLeft.y` | number |  |
| `fields.expirationDate.location.topRight.x` | number |  |
| `fields.expirationDate.location.topRight.y` | number |  |
| `fields.expirationDate.ocrText` | string |  |
| `fields.expirationDate.type` | string |  |
| `fields.expirationDate.value` | string |  |
| `fields.familyName.confidence` | number |  |
| `fields.familyName.key` | string |  |
| `fields.familyName.location.bottomLeft.x` | number |  |
| `fields.familyName.location.bottomLeft.y` | number |  |
| `fields.familyName.location.bottomRight.x` | number |  |
| `fields.familyName.location.bottomRight.y` | number |  |
| `fields.familyName.location.pageNumber` | number |  |
| `fields.familyName.location.topLeft.x` | number |  |
| `fields.familyName.location.topLeft.y` | number |  |
| `fields.familyName.location.topRight.x` | number |  |
| `fields.familyName.location.topRight.y` | number |  |
| `fields.familyName.value` | string |  |
| `fields.familyNameLocal.confidence` | number |  |
| `fields.familyNameLocal.key` | string |  |
| `fields.familyNameLocal.location.bottomLeft.x` | number |  |
| `fields.familyNameLocal.location.bottomLeft.y` | number |  |
| `fields.familyNameLocal.location.bottomRight.x` | number |  |
| `fields.familyNameLocal.location.bottomRight.y` | number |  |
| `fields.familyNameLocal.location.pageNumber` | number |  |
| `fields.familyNameLocal.location.topLeft.x` | number |  |
| `fields.familyNameLocal.location.topLeft.y` | number |  |
| `fields.familyNameLocal.location.topRight.x` | number |  |
| `fields.familyNameLocal.location.topRight.y` | number |  |
| `fields.familyNameLocal.value` | string |  |
| `fields.givenName.confidence` | number |  |
| `fields.givenName.key` | string |  |
| `fields.givenName.location.bottomLeft.x` | number |  |
| `fields.givenName.location.bottomLeft.y` | number |  |
| `fields.givenName.location.bottomRight.x` | number |  |
| `fields.givenName.location.bottomRight.y` | number |  |
| `fields.givenName.location.pageNumber` | number |  |
| `fields.givenName.location.topLeft.x` | number |  |
| `fields.givenName.location.topLeft.y` | number |  |
| `fields.givenName.location.topRight.x` | number |  |
| `fields.givenName.location.topRight.y` | number |  |
| `fields.givenName.value` | string |  |
| `fields.givenNameLocal.confidence` | number |  |
| `fields.givenNameLocal.key` | string |  |
| `fields.givenNameLocal.location.bottomLeft.x` | number |  |
| `fields.givenNameLocal.location.bottomLeft.y` | number |  |
| `fields.givenNameLocal.location.bottomRight.x` | number |  |
| `fields.givenNameLocal.location.bottomRight.y` | number |  |
| `fields.givenNameLocal.location.pageNumber` | number |  |
| `fields.givenNameLocal.location.topLeft.x` | number |  |
| `fields.givenNameLocal.location.topLeft.y` | number |  |
| `fields.givenNameLocal.location.topRight.x` | number |  |
| `fields.givenNameLocal.location.topRight.y` | number |  |
| `fields.givenNameLocal.value` | string |  |
| `fields.issueDate.confidence` | number |  |
| `fields.issueDate.isValid` | boolean |  |
| `fields.issueDate.key` | string |  |
| `fields.issueDate.location.bottomLeft.x` | number |  |
| `fields.issueDate.location.bottomLeft.y` | number |  |
| `fields.issueDate.location.bottomRight.x` | number |  |
| `fields.issueDate.location.bottomRight.y` | number |  |
| `fields.issueDate.location.pageNumber` | number |  |
| `fields.issueDate.location.topLeft.x` | number |  |
| `fields.issueDate.location.topLeft.y` | number |  |
| `fields.issueDate.location.topRight.x` | number |  |
| `fields.issueDate.location.topRight.y` | number |  |
| `fields.issueDate.ocrText` | string |  |
| `fields.issueDate.value` | string |  |
| `fields.issuingState.confidence` | number |  |
| `fields.issuingState.key` | string |  |
| `fields.issuingState.location.bottomLeft.x` | number |  |
| `fields.issuingState.location.bottomLeft.y` | number |  |
| `fields.issuingState.location.bottomRight.x` | number |  |
| `fields.issuingState.location.bottomRight.y` | number |  |
| `fields.issuingState.location.pageNumber` | number |  |
| `fields.issuingState.location.topLeft.x` | number |  |
| `fields.issuingState.location.topLeft.y` | number |  |
| `fields.issuingState.location.topRight.x` | number |  |
| `fields.issuingState.location.topRight.y` | number |  |
| `fields.issuingState.value` | string |  |
| `fields.nationality.confidence` | number |  |
| `fields.nationality.key` | string |  |
| `fields.nationality.location.bottomLeft.x` | number |  |
| `fields.nationality.location.bottomLeft.y` | number |  |
| `fields.nationality.location.bottomRight.x` | number |  |
| `fields.nationality.location.bottomRight.y` | number |  |
| `fields.nationality.location.pageNumber` | number |  |
| `fields.nationality.location.topLeft.x` | number |  |
| `fields.nationality.location.topLeft.y` | number |  |
| `fields.nationality.location.topRight.x` | number |  |
| `fields.nationality.location.topRight.y` | number |  |
| `fields.nationality.value` | string |  |
| `fields.personalNumber.confidence` | number |  |
| `fields.personalNumber.key` | string |  |
| `fields.personalNumber.location.bottomLeft.x` | number |  |
| `fields.personalNumber.location.bottomLeft.y` | number |  |
| `fields.personalNumber.location.bottomRight.x` | number |  |
| `fields.personalNumber.location.bottomRight.y` | number |  |
| `fields.personalNumber.location.pageNumber` | number |  |
| `fields.personalNumber.location.topLeft.x` | number |  |
| `fields.personalNumber.location.topLeft.y` | number |  |
| `fields.personalNumber.location.topRight.x` | number |  |
| `fields.personalNumber.location.topRight.y` | number |  |
| `fields.personalNumber.value` | string |  |
| `fields.placeOfBirth.confidence` | number |  |
| `fields.placeOfBirth.key` | string |  |
| `fields.placeOfBirth.location.bottomLeft.x` | number |  |
| `fields.placeOfBirth.location.bottomLeft.y` | number |  |
| `fields.placeOfBirth.location.bottomRight.x` | number |  |
| `fields.placeOfBirth.location.bottomRight.y` | number |  |
| `fields.placeOfBirth.location.pageNumber` | number |  |
| `fields.placeOfBirth.location.topLeft.x` | number |  |
| `fields.placeOfBirth.location.topLeft.y` | number |  |
| `fields.placeOfBirth.location.topRight.x` | number |  |
| `fields.placeOfBirth.location.topRight.y` | number |  |
| `fields.placeOfBirth.value` | string |  |
| `fields.sex.confidence` | number |  |
| `fields.sex.key` | string |  |
| `fields.sex.location.bottomLeft.x` | number |  |
| `fields.sex.location.bottomLeft.y` | number |  |
| `fields.sex.location.bottomRight.x` | number |  |
| `fields.sex.location.bottomRight.y` | number |  |
| `fields.sex.location.pageNumber` | number |  |
| `fields.sex.location.topLeft.x` | number |  |
| `fields.sex.location.topLeft.y` | number |  |
| `fields.sex.location.topRight.x` | number |  |
| `fields.sex.location.topRight.y` | number |  |
| `fields.sex.value` | string |  |
| `model.confidence` | number |  |
| `model.isValid` | boolean |  |
| `model.name` | string |  |
| `model.shape` | string |  |
| `model.type` | string |  |
| `ocr` | string |  |
| `status` | string |  |
| `uuid` | string |  |

## Native endpoint

Through the native Base64.ai API, this operation is `GET /api/scan/async/:asyncFileUUID` (base URL `https://base64.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-asynchronous-scan-result.md) for the provider-specific parameters and requirements.

