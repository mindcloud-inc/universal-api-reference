# Base64.ai: Mock Document Extraction

Creates a mock extraction result in Base64.ai.

```
POST https://connect.mindcloud.co/v1/universal/base64ai/latest/actions/mock-document-extraction
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Base64.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/base64ai/latest/actions/mock-document-extraction" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "document": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/base64ai/latest/actions/mock-document-extraction', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "document": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `document` | string | yes | Base64-encoded document or image payload for the mock endpoint. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "features": {
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
        "properties": {
          "height": 1,
          "isGlareFree": true,
          "isInFocus": true,
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
        ],
        "textToSpeech": "string"
      },
      "fields": {
        "address": {
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
        "age": {
          "confidence": 1,
          "isValid": true,
          "key": "string",
          "type": "string",
          "value": 1
        },
        "class": {
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
        "documentType": {
          "confidence": 1,
          "isValid": true,
          "key": "string",
          "type": "string",
          "value": "string"
        },
        "driverLicenseType": {
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
        "isEnhancedId": {
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
          "type": "string",
          "value": "string"
        },
        "isFrontSide": {
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
          "type": "string",
          "value": "string"
        },
        "isRealId": {
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
          "type": "string",
          "value": "string"
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
          "type": "string",
          "value": "string"
        },
        "licenseNumber": {
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
          "value": "string"
        },
        "sex": {
          "confidence": 1,
          "isValid": true,
          "key": "string",
          "value": "string"
        },
        "stateCode": {
          "confidence": 1,
          "key": "string",
          "type": "string",
          "value": "string"
        },
        "stateName": {
          "confidence": 1,
          "isValid": true,
          "key": "Ava Chen",
          "type": "Ava Chen",
          "value": "Ava Chen"
        }
      },
      "model": {
        "confidence": 1,
        "isValid": true,
        "name": "Ava Chen",
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
| `features.properties.height` | number |  |
| `features.properties.isGlareFree` | boolean |  |
| `features.properties.isInFocus` | boolean |  |
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
| `features.textToSpeech` | string |  |
| `fields.address.confidence` | number |  |
| `fields.address.key` | string |  |
| `fields.address.location.bottomLeft.x` | number |  |
| `fields.address.location.bottomLeft.y` | number |  |
| `fields.address.location.bottomRight.x` | number |  |
| `fields.address.location.bottomRight.y` | number |  |
| `fields.address.location.pageNumber` | number |  |
| `fields.address.location.topLeft.x` | number |  |
| `fields.address.location.topLeft.y` | number |  |
| `fields.address.location.topRight.x` | number |  |
| `fields.address.location.topRight.y` | number |  |
| `fields.address.value` | string |  |
| `fields.age.confidence` | number |  |
| `fields.age.isValid` | boolean |  |
| `fields.age.key` | string |  |
| `fields.age.type` | string |  |
| `fields.age.value` | number |  |
| `fields.class.confidence` | number |  |
| `fields.class.key` | string |  |
| `fields.class.location.bottomLeft.x` | number |  |
| `fields.class.location.bottomLeft.y` | number |  |
| `fields.class.location.bottomRight.x` | number |  |
| `fields.class.location.bottomRight.y` | number |  |
| `fields.class.location.pageNumber` | number |  |
| `fields.class.location.topLeft.x` | number |  |
| `fields.class.location.topLeft.y` | number |  |
| `fields.class.location.topRight.x` | number |  |
| `fields.class.location.topRight.y` | number |  |
| `fields.class.value` | string |  |
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
| `fields.documentType.confidence` | number |  |
| `fields.documentType.isValid` | boolean |  |
| `fields.documentType.key` | string |  |
| `fields.documentType.type` | string |  |
| `fields.documentType.value` | string |  |
| `fields.driverLicenseType.confidence` | number |  |
| `fields.driverLicenseType.key` | string |  |
| `fields.driverLicenseType.location.bottomLeft.x` | number |  |
| `fields.driverLicenseType.location.bottomLeft.y` | number |  |
| `fields.driverLicenseType.location.bottomRight.x` | number |  |
| `fields.driverLicenseType.location.bottomRight.y` | number |  |
| `fields.driverLicenseType.location.pageNumber` | number |  |
| `fields.driverLicenseType.location.topLeft.x` | number |  |
| `fields.driverLicenseType.location.topLeft.y` | number |  |
| `fields.driverLicenseType.location.topRight.x` | number |  |
| `fields.driverLicenseType.location.topRight.y` | number |  |
| `fields.driverLicenseType.value` | string |  |
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
| `fields.isEnhancedId.confidence` | number |  |
| `fields.isEnhancedId.key` | string |  |
| `fields.isEnhancedId.location.bottomLeft.x` | number |  |
| `fields.isEnhancedId.location.bottomLeft.y` | number |  |
| `fields.isEnhancedId.location.bottomRight.x` | number |  |
| `fields.isEnhancedId.location.bottomRight.y` | number |  |
| `fields.isEnhancedId.location.pageNumber` | number |  |
| `fields.isEnhancedId.location.topLeft.x` | number |  |
| `fields.isEnhancedId.location.topLeft.y` | number |  |
| `fields.isEnhancedId.location.topRight.x` | number |  |
| `fields.isEnhancedId.location.topRight.y` | number |  |
| `fields.isEnhancedId.type` | string |  |
| `fields.isEnhancedId.value` | string |  |
| `fields.isFrontSide.confidence` | number |  |
| `fields.isFrontSide.isValid` | boolean |  |
| `fields.isFrontSide.key` | string |  |
| `fields.isFrontSide.location.bottomLeft.x` | number |  |
| `fields.isFrontSide.location.bottomLeft.y` | number |  |
| `fields.isFrontSide.location.bottomRight.x` | number |  |
| `fields.isFrontSide.location.bottomRight.y` | number |  |
| `fields.isFrontSide.location.pageNumber` | number |  |
| `fields.isFrontSide.location.topLeft.x` | number |  |
| `fields.isFrontSide.location.topLeft.y` | number |  |
| `fields.isFrontSide.location.topRight.x` | number |  |
| `fields.isFrontSide.location.topRight.y` | number |  |
| `fields.isFrontSide.type` | string |  |
| `fields.isFrontSide.value` | string |  |
| `fields.isRealId.confidence` | number |  |
| `fields.isRealId.key` | string |  |
| `fields.isRealId.location.bottomLeft.x` | number |  |
| `fields.isRealId.location.bottomLeft.y` | number |  |
| `fields.isRealId.location.bottomRight.x` | number |  |
| `fields.isRealId.location.bottomRight.y` | number |  |
| `fields.isRealId.location.pageNumber` | number |  |
| `fields.isRealId.location.topLeft.x` | number |  |
| `fields.isRealId.location.topLeft.y` | number |  |
| `fields.isRealId.location.topRight.x` | number |  |
| `fields.isRealId.location.topRight.y` | number |  |
| `fields.isRealId.type` | string |  |
| `fields.isRealId.value` | string |  |
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
| `fields.issueDate.type` | string |  |
| `fields.issueDate.value` | string |  |
| `fields.licenseNumber.confidence` | number |  |
| `fields.licenseNumber.isValid` | boolean |  |
| `fields.licenseNumber.key` | string |  |
| `fields.licenseNumber.location.bottomLeft.x` | number |  |
| `fields.licenseNumber.location.bottomLeft.y` | number |  |
| `fields.licenseNumber.location.bottomRight.x` | number |  |
| `fields.licenseNumber.location.bottomRight.y` | number |  |
| `fields.licenseNumber.location.pageNumber` | number |  |
| `fields.licenseNumber.location.topLeft.x` | number |  |
| `fields.licenseNumber.location.topLeft.y` | number |  |
| `fields.licenseNumber.location.topRight.x` | number |  |
| `fields.licenseNumber.location.topRight.y` | number |  |
| `fields.licenseNumber.value` | string |  |
| `fields.sex.confidence` | number |  |
| `fields.sex.isValid` | boolean |  |
| `fields.sex.key` | string |  |
| `fields.sex.value` | string |  |
| `fields.stateCode.confidence` | number |  |
| `fields.stateCode.key` | string |  |
| `fields.stateCode.type` | string |  |
| `fields.stateCode.value` | string |  |
| `fields.stateName.confidence` | number |  |
| `fields.stateName.isValid` | boolean |  |
| `fields.stateName.key` | string |  |
| `fields.stateName.type` | string |  |
| `fields.stateName.value` | string |  |
| `model.confidence` | number |  |
| `model.isValid` | boolean |  |
| `model.name` | string |  |
| `model.type` | string |  |
| `ocr` | string |  |
| `status` | string |  |
| `uuid` | string |  |

## Native endpoint

Through the native Base64.ai API, this operation is `POST /mock/scan` (base URL `https://base64.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/mock-document-extraction.md) for the provider-specific parameters and requirements.

