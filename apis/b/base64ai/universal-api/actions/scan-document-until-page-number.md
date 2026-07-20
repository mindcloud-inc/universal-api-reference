# Base64.ai: Scan Document Until Page Number

Creates a Base64.ai scan result up to a specified page number.

```
POST https://connect.mindcloud.co/v1/universal/base64ai/latest/actions/scan-document-until-page-number
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Base64.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/base64ai/latest/actions/scan-document-until-page-number" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/base64ai/latest/actions/scan-document-until-page-number', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "url": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `url` | string | yes | Public URL of the document to scan with a page limit. |
| `settings` | object | no | Scan settings object, for example {"limitPages":1}. Default: `{"limitPages":1}`. |

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
                "originalDocumentEndPage": 1,
                "rotationAngle": 1,
                "width": 1
              },
              "tables": [
                {
                  "blocks": {
                    "after": {
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
                    },
                    "before": {
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
                  },
                  "box": {
                    "bottom": 1,
                    "height": 1,
                    "left": 1,
                    "pageNumber": 1,
                    "right": 1,
                    "top": 1,
                    "width": 1
                  },
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
                  "rows": [
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
                      "cells": [
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
                  "text": "string",
                  "title": "string"
                }
              ],
              "text": "string"
            }
          ],
          "text": "string"
        },
        "fraud": {
          "indicators": [
            {
              "category": "string",
              "confidence": "string",
              "description": "string",
              "evidences": [
                {
                  "revisionCount": "string"
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
          "originalDocumentEndPage": 1,
          "originalFileName": "Ava Chen",
          "pageCount": 1,
          "rotationAngle": 1,
          "startPage": 1,
          "width": 1
        },
        "tables": [
          {}
        ]
      },
      "fields": {
        "carrierName": {
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
        "coverageEnd": {
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
        "coverageFor": {
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
          "ocrText": "string",
          "value": "string"
        },
        "coverageStart": {
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
        "phoneNumber": {
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
        "planName": {
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
          "ocrText": "Ava Chen",
          "value": "Ava Chen"
        },
        "planTypeFull": {
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
          "ocrText": "string",
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
| `features.creditsSpent` | number |  |
| `features.dom.box.bottom` | number |  |
| `features.dom.box.height` | number |  |
| `features.dom.box.left` | number |  |
| `features.dom.box.pageNumber` | object |  |
| `features.dom.box.right` | number |  |
| `features.dom.box.top` | number |  |
| `features.dom.box.width` | number |  |
| `features.dom.confidence` | number |  |
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
| `features.dom.pages[].properties.originalDocumentEndPage` | number |  |
| `features.dom.pages[].properties.rotationAngle` | number |  |
| `features.dom.pages[].properties.width` | number |  |
| `features.dom.pages[].tables[].blocks.after.box.bottom` | number |  |
| `features.dom.pages[].tables[].blocks.after.box.height` | number |  |
| `features.dom.pages[].tables[].blocks.after.box.left` | number |  |
| `features.dom.pages[].tables[].blocks.after.box.pageNumber` | number |  |
| `features.dom.pages[].tables[].blocks.after.box.right` | number |  |
| `features.dom.pages[].tables[].blocks.after.box.top` | number |  |
| `features.dom.pages[].tables[].blocks.after.box.width` | number |  |
| `features.dom.pages[].tables[].blocks.after.confidence` | number |  |
| `features.dom.pages[].tables[].blocks.after.lines[].box.bottom` | number |  |
| `features.dom.pages[].tables[].blocks.after.lines[].box.height` | number |  |
| `features.dom.pages[].tables[].blocks.after.lines[].box.left` | number |  |
| `features.dom.pages[].tables[].blocks.after.lines[].box.pageNumber` | number |  |
| `features.dom.pages[].tables[].blocks.after.lines[].box.right` | number |  |
| `features.dom.pages[].tables[].blocks.after.lines[].box.top` | number |  |
| `features.dom.pages[].tables[].blocks.after.lines[].box.width` | number |  |
| `features.dom.pages[].tables[].blocks.after.lines[].confidence` | number |  |
| `features.dom.pages[].tables[].blocks.after.lines[].location.bottomLeft.x` | number |  |
| `features.dom.pages[].tables[].blocks.after.lines[].location.bottomLeft.y` | number |  |
| `features.dom.pages[].tables[].blocks.after.lines[].location.bottomRight.x` | number |  |
| `features.dom.pages[].tables[].blocks.after.lines[].location.bottomRight.y` | number |  |
| `features.dom.pages[].tables[].blocks.after.lines[].location.pageNumber` | number |  |
| `features.dom.pages[].tables[].blocks.after.lines[].location.topLeft.x` | number |  |
| `features.dom.pages[].tables[].blocks.after.lines[].location.topLeft.y` | number |  |
| `features.dom.pages[].tables[].blocks.after.lines[].location.topRight.x` | number |  |
| `features.dom.pages[].tables[].blocks.after.lines[].location.topRight.y` | number |  |
| `features.dom.pages[].tables[].blocks.after.lines[].text` | string |  |
| `features.dom.pages[].tables[].blocks.after.lines[].words[].box.bottom` | number |  |
| `features.dom.pages[].tables[].blocks.after.lines[].words[].box.height` | number |  |
| `features.dom.pages[].tables[].blocks.after.lines[].words[].box.left` | number |  |
| `features.dom.pages[].tables[].blocks.after.lines[].words[].box.pageNumber` | number |  |
| `features.dom.pages[].tables[].blocks.after.lines[].words[].box.right` | number |  |
| `features.dom.pages[].tables[].blocks.after.lines[].words[].box.top` | number |  |
| `features.dom.pages[].tables[].blocks.after.lines[].words[].box.width` | number |  |
| `features.dom.pages[].tables[].blocks.after.lines[].words[].confidence` | number |  |
| `features.dom.pages[].tables[].blocks.after.lines[].words[].location.bottomLeft.x` | number |  |
| `features.dom.pages[].tables[].blocks.after.lines[].words[].location.bottomLeft.y` | number |  |
| `features.dom.pages[].tables[].blocks.after.lines[].words[].location.bottomRight.x` | number |  |
| `features.dom.pages[].tables[].blocks.after.lines[].words[].location.bottomRight.y` | number |  |
| `features.dom.pages[].tables[].blocks.after.lines[].words[].location.pageNumber` | number |  |
| `features.dom.pages[].tables[].blocks.after.lines[].words[].location.topLeft.x` | number |  |
| `features.dom.pages[].tables[].blocks.after.lines[].words[].location.topLeft.y` | number |  |
| `features.dom.pages[].tables[].blocks.after.lines[].words[].location.topRight.x` | number |  |
| `features.dom.pages[].tables[].blocks.after.lines[].words[].location.topRight.y` | number |  |
| `features.dom.pages[].tables[].blocks.after.lines[].words[].text` | string |  |
| `features.dom.pages[].tables[].blocks.after.location.bottomLeft.x` | number |  |
| `features.dom.pages[].tables[].blocks.after.location.bottomLeft.y` | number |  |
| `features.dom.pages[].tables[].blocks.after.location.bottomRight.x` | number |  |
| `features.dom.pages[].tables[].blocks.after.location.bottomRight.y` | number |  |
| `features.dom.pages[].tables[].blocks.after.location.pageNumber` | number |  |
| `features.dom.pages[].tables[].blocks.after.location.topLeft.x` | number |  |
| `features.dom.pages[].tables[].blocks.after.location.topLeft.y` | number |  |
| `features.dom.pages[].tables[].blocks.after.location.topRight.x` | number |  |
| `features.dom.pages[].tables[].blocks.after.location.topRight.y` | number |  |
| `features.dom.pages[].tables[].blocks.after.text` | string |  |
| `features.dom.pages[].tables[].blocks.before.box.bottom` | number |  |
| `features.dom.pages[].tables[].blocks.before.box.height` | number |  |
| `features.dom.pages[].tables[].blocks.before.box.left` | number |  |
| `features.dom.pages[].tables[].blocks.before.box.pageNumber` | number |  |
| `features.dom.pages[].tables[].blocks.before.box.right` | number |  |
| `features.dom.pages[].tables[].blocks.before.box.top` | number |  |
| `features.dom.pages[].tables[].blocks.before.box.width` | number |  |
| `features.dom.pages[].tables[].blocks.before.confidence` | number |  |
| `features.dom.pages[].tables[].blocks.before.lines[].box.bottom` | number |  |
| `features.dom.pages[].tables[].blocks.before.lines[].box.height` | number |  |
| `features.dom.pages[].tables[].blocks.before.lines[].box.left` | number |  |
| `features.dom.pages[].tables[].blocks.before.lines[].box.pageNumber` | number |  |
| `features.dom.pages[].tables[].blocks.before.lines[].box.right` | number |  |
| `features.dom.pages[].tables[].blocks.before.lines[].box.top` | number |  |
| `features.dom.pages[].tables[].blocks.before.lines[].box.width` | number |  |
| `features.dom.pages[].tables[].blocks.before.lines[].confidence` | number |  |
| `features.dom.pages[].tables[].blocks.before.lines[].location.bottomLeft.x` | number |  |
| `features.dom.pages[].tables[].blocks.before.lines[].location.bottomLeft.y` | number |  |
| `features.dom.pages[].tables[].blocks.before.lines[].location.bottomRight.x` | number |  |
| `features.dom.pages[].tables[].blocks.before.lines[].location.bottomRight.y` | number |  |
| `features.dom.pages[].tables[].blocks.before.lines[].location.pageNumber` | number |  |
| `features.dom.pages[].tables[].blocks.before.lines[].location.topLeft.x` | number |  |
| `features.dom.pages[].tables[].blocks.before.lines[].location.topLeft.y` | number |  |
| `features.dom.pages[].tables[].blocks.before.lines[].location.topRight.x` | number |  |
| `features.dom.pages[].tables[].blocks.before.lines[].location.topRight.y` | number |  |
| `features.dom.pages[].tables[].blocks.before.lines[].text` | string |  |
| `features.dom.pages[].tables[].blocks.before.lines[].words[].box.bottom` | number |  |
| `features.dom.pages[].tables[].blocks.before.lines[].words[].box.height` | number |  |
| `features.dom.pages[].tables[].blocks.before.lines[].words[].box.left` | number |  |
| `features.dom.pages[].tables[].blocks.before.lines[].words[].box.pageNumber` | number |  |
| `features.dom.pages[].tables[].blocks.before.lines[].words[].box.right` | number |  |
| `features.dom.pages[].tables[].blocks.before.lines[].words[].box.top` | number |  |
| `features.dom.pages[].tables[].blocks.before.lines[].words[].box.width` | number |  |
| `features.dom.pages[].tables[].blocks.before.lines[].words[].confidence` | number |  |
| `features.dom.pages[].tables[].blocks.before.lines[].words[].location.bottomLeft.x` | number |  |
| `features.dom.pages[].tables[].blocks.before.lines[].words[].location.bottomLeft.y` | number |  |
| `features.dom.pages[].tables[].blocks.before.lines[].words[].location.bottomRight.x` | number |  |
| `features.dom.pages[].tables[].blocks.before.lines[].words[].location.bottomRight.y` | number |  |
| `features.dom.pages[].tables[].blocks.before.lines[].words[].location.pageNumber` | number |  |
| `features.dom.pages[].tables[].blocks.before.lines[].words[].location.topLeft.x` | number |  |
| `features.dom.pages[].tables[].blocks.before.lines[].words[].location.topLeft.y` | number |  |
| `features.dom.pages[].tables[].blocks.before.lines[].words[].location.topRight.x` | number |  |
| `features.dom.pages[].tables[].blocks.before.lines[].words[].location.topRight.y` | number |  |
| `features.dom.pages[].tables[].blocks.before.lines[].words[].text` | string |  |
| `features.dom.pages[].tables[].blocks.before.location.bottomLeft.x` | number |  |
| `features.dom.pages[].tables[].blocks.before.location.bottomLeft.y` | number |  |
| `features.dom.pages[].tables[].blocks.before.location.bottomRight.x` | number |  |
| `features.dom.pages[].tables[].blocks.before.location.bottomRight.y` | number |  |
| `features.dom.pages[].tables[].blocks.before.location.pageNumber` | number |  |
| `features.dom.pages[].tables[].blocks.before.location.topLeft.x` | number |  |
| `features.dom.pages[].tables[].blocks.before.location.topLeft.y` | number |  |
| `features.dom.pages[].tables[].blocks.before.location.topRight.x` | number |  |
| `features.dom.pages[].tables[].blocks.before.location.topRight.y` | number |  |
| `features.dom.pages[].tables[].blocks.before.text` | string |  |
| `features.dom.pages[].tables[].box.bottom` | number |  |
| `features.dom.pages[].tables[].box.height` | number |  |
| `features.dom.pages[].tables[].box.left` | number |  |
| `features.dom.pages[].tables[].box.pageNumber` | number |  |
| `features.dom.pages[].tables[].box.right` | number |  |
| `features.dom.pages[].tables[].box.top` | number |  |
| `features.dom.pages[].tables[].box.width` | number |  |
| `features.dom.pages[].tables[].location.bottomLeft.x` | number |  |
| `features.dom.pages[].tables[].location.bottomLeft.y` | number |  |
| `features.dom.pages[].tables[].location.bottomRight.x` | number |  |
| `features.dom.pages[].tables[].location.bottomRight.y` | number |  |
| `features.dom.pages[].tables[].location.pageNumber` | number |  |
| `features.dom.pages[].tables[].location.topLeft.x` | number |  |
| `features.dom.pages[].tables[].location.topLeft.y` | number |  |
| `features.dom.pages[].tables[].location.topRight.x` | number |  |
| `features.dom.pages[].tables[].location.topRight.y` | number |  |
| `features.dom.pages[].tables[].rows[].box.bottom` | number |  |
| `features.dom.pages[].tables[].rows[].box.height` | number |  |
| `features.dom.pages[].tables[].rows[].box.left` | number |  |
| `features.dom.pages[].tables[].rows[].box.pageNumber` | number |  |
| `features.dom.pages[].tables[].rows[].box.right` | number |  |
| `features.dom.pages[].tables[].rows[].box.top` | number |  |
| `features.dom.pages[].tables[].rows[].box.width` | number |  |
| `features.dom.pages[].tables[].rows[].cells[].box.bottom` | number |  |
| `features.dom.pages[].tables[].rows[].cells[].box.height` | number |  |
| `features.dom.pages[].tables[].rows[].cells[].box.left` | number |  |
| `features.dom.pages[].tables[].rows[].cells[].box.pageNumber` | number |  |
| `features.dom.pages[].tables[].rows[].cells[].box.right` | number |  |
| `features.dom.pages[].tables[].rows[].cells[].box.top` | number |  |
| `features.dom.pages[].tables[].rows[].cells[].box.width` | number |  |
| `features.dom.pages[].tables[].rows[].cells[].confidence` | number |  |
| `features.dom.pages[].tables[].rows[].cells[].location.bottomLeft.x` | number |  |
| `features.dom.pages[].tables[].rows[].cells[].location.bottomLeft.y` | number |  |
| `features.dom.pages[].tables[].rows[].cells[].location.bottomRight.x` | number |  |
| `features.dom.pages[].tables[].rows[].cells[].location.bottomRight.y` | number |  |
| `features.dom.pages[].tables[].rows[].cells[].location.pageNumber` | number |  |
| `features.dom.pages[].tables[].rows[].cells[].location.topLeft.x` | number |  |
| `features.dom.pages[].tables[].rows[].cells[].location.topLeft.y` | number |  |
| `features.dom.pages[].tables[].rows[].cells[].location.topRight.x` | number |  |
| `features.dom.pages[].tables[].rows[].cells[].location.topRight.y` | number |  |
| `features.dom.pages[].tables[].rows[].cells[].text` | string |  |
| `features.dom.pages[].tables[].rows[].location.bottomLeft.x` | number |  |
| `features.dom.pages[].tables[].rows[].location.bottomLeft.y` | number |  |
| `features.dom.pages[].tables[].rows[].location.bottomRight.x` | number |  |
| `features.dom.pages[].tables[].rows[].location.bottomRight.y` | number |  |
| `features.dom.pages[].tables[].rows[].location.pageNumber` | number |  |
| `features.dom.pages[].tables[].rows[].location.topLeft.x` | number |  |
| `features.dom.pages[].tables[].rows[].location.topLeft.y` | number |  |
| `features.dom.pages[].tables[].rows[].location.topRight.x` | number |  |
| `features.dom.pages[].tables[].rows[].location.topRight.y` | number |  |
| `features.dom.pages[].tables[].rows[].text` | string |  |
| `features.dom.pages[].tables[].text` | string |  |
| `features.dom.pages[].tables[].title` | string |  |
| `features.dom.pages[].text` | string |  |
| `features.dom.text` | string |  |
| `features.fraud.indicators[].category` | string |  |
| `features.fraud.indicators[].confidence` | string |  |
| `features.fraud.indicators[].description` | string |  |
| `features.fraud.indicators[].evidences[].revisionCount` | string |  |
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
| `features.properties.originalDocumentEndPage` | number |  |
| `features.properties.originalFileName` | string |  |
| `features.properties.pageCount` | number |  |
| `features.properties.rotationAngle` | number |  |
| `features.properties.startPage` | number |  |
| `features.properties.width` | number |  |
| `features.tables[]` | object |  |
| `fields.carrierName.confidence` | number |  |
| `fields.carrierName.key` | string |  |
| `fields.carrierName.location.bottomLeft.x` | number |  |
| `fields.carrierName.location.bottomLeft.y` | number |  |
| `fields.carrierName.location.bottomRight.x` | number |  |
| `fields.carrierName.location.bottomRight.y` | number |  |
| `fields.carrierName.location.pageNumber` | number |  |
| `fields.carrierName.location.topLeft.x` | number |  |
| `fields.carrierName.location.topLeft.y` | number |  |
| `fields.carrierName.location.topRight.x` | number |  |
| `fields.carrierName.location.topRight.y` | number |  |
| `fields.carrierName.value` | string |  |
| `fields.coverageEnd.confidence` | number |  |
| `fields.coverageEnd.isValid` | boolean |  |
| `fields.coverageEnd.key` | string |  |
| `fields.coverageEnd.location.bottomLeft.x` | number |  |
| `fields.coverageEnd.location.bottomLeft.y` | number |  |
| `fields.coverageEnd.location.bottomRight.x` | number |  |
| `fields.coverageEnd.location.bottomRight.y` | number |  |
| `fields.coverageEnd.location.pageNumber` | number |  |
| `fields.coverageEnd.location.topLeft.x` | number |  |
| `fields.coverageEnd.location.topLeft.y` | number |  |
| `fields.coverageEnd.location.topRight.x` | number |  |
| `fields.coverageEnd.location.topRight.y` | number |  |
| `fields.coverageEnd.ocrText` | string |  |
| `fields.coverageEnd.value` | string |  |
| `fields.coverageFor.confidence` | number |  |
| `fields.coverageFor.key` | string |  |
| `fields.coverageFor.location.bottomLeft.x` | number |  |
| `fields.coverageFor.location.bottomLeft.y` | number |  |
| `fields.coverageFor.location.bottomRight.x` | number |  |
| `fields.coverageFor.location.bottomRight.y` | number |  |
| `fields.coverageFor.location.pageNumber` | number |  |
| `fields.coverageFor.location.topLeft.x` | number |  |
| `fields.coverageFor.location.topLeft.y` | number |  |
| `fields.coverageFor.location.topRight.x` | number |  |
| `fields.coverageFor.location.topRight.y` | number |  |
| `fields.coverageFor.ocrText` | string |  |
| `fields.coverageFor.value` | string |  |
| `fields.coverageStart.confidence` | number |  |
| `fields.coverageStart.isValid` | boolean |  |
| `fields.coverageStart.key` | string |  |
| `fields.coverageStart.location.bottomLeft.x` | number |  |
| `fields.coverageStart.location.bottomLeft.y` | number |  |
| `fields.coverageStart.location.bottomRight.x` | number |  |
| `fields.coverageStart.location.bottomRight.y` | number |  |
| `fields.coverageStart.location.pageNumber` | number |  |
| `fields.coverageStart.location.topLeft.x` | number |  |
| `fields.coverageStart.location.topLeft.y` | number |  |
| `fields.coverageStart.location.topRight.x` | number |  |
| `fields.coverageStart.location.topRight.y` | number |  |
| `fields.coverageStart.ocrText` | string |  |
| `fields.coverageStart.value` | string |  |
| `fields.phoneNumber.confidence` | number |  |
| `fields.phoneNumber.key` | string |  |
| `fields.phoneNumber.location.bottomLeft.x` | number |  |
| `fields.phoneNumber.location.bottomLeft.y` | number |  |
| `fields.phoneNumber.location.bottomRight.x` | number |  |
| `fields.phoneNumber.location.bottomRight.y` | number |  |
| `fields.phoneNumber.location.pageNumber` | number |  |
| `fields.phoneNumber.location.topLeft.x` | number |  |
| `fields.phoneNumber.location.topLeft.y` | number |  |
| `fields.phoneNumber.location.topRight.x` | number |  |
| `fields.phoneNumber.location.topRight.y` | number |  |
| `fields.phoneNumber.value` | string |  |
| `fields.planName.confidence` | number |  |
| `fields.planName.key` | string |  |
| `fields.planName.location.bottomLeft.x` | number |  |
| `fields.planName.location.bottomLeft.y` | number |  |
| `fields.planName.location.bottomRight.x` | number |  |
| `fields.planName.location.bottomRight.y` | number |  |
| `fields.planName.location.pageNumber` | number |  |
| `fields.planName.location.topLeft.x` | number |  |
| `fields.planName.location.topLeft.y` | number |  |
| `fields.planName.location.topRight.x` | number |  |
| `fields.planName.location.topRight.y` | number |  |
| `fields.planName.ocrText` | string |  |
| `fields.planName.value` | string |  |
| `fields.planTypeFull.confidence` | number |  |
| `fields.planTypeFull.key` | string |  |
| `fields.planTypeFull.location.bottomLeft.x` | number |  |
| `fields.planTypeFull.location.bottomLeft.y` | number |  |
| `fields.planTypeFull.location.bottomRight.x` | number |  |
| `fields.planTypeFull.location.bottomRight.y` | number |  |
| `fields.planTypeFull.location.pageNumber` | number |  |
| `fields.planTypeFull.location.topLeft.x` | number |  |
| `fields.planTypeFull.location.topLeft.y` | number |  |
| `fields.planTypeFull.location.topRight.x` | number |  |
| `fields.planTypeFull.location.topRight.y` | number |  |
| `fields.planTypeFull.ocrText` | string |  |
| `fields.planTypeFull.value` | string |  |
| `model.confidence` | number |  |
| `model.isValid` | boolean |  |
| `model.name` | string |  |
| `model.shape` | string |  |
| `model.type` | string |  |
| `ocr` | string |  |
| `status` | string |  |
| `uuid` | string |  |

## Native endpoint

Through the native Base64.ai API, this operation is `POST /api/scan` (base URL `https://base64.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/scan-document-until-page-number.md) for the provider-specific parameters and requirements.

