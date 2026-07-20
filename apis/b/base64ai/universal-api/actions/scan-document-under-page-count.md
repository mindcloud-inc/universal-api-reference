# Base64.ai: Scan Document Under Page Count

Creates a Base64.ai scan result for documents under a page limit.

```
POST https://connect.mindcloud.co/v1/universal/base64ai/latest/actions/scan-document-under-page-count
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Base64.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/base64ai/latest/actions/scan-document-under-page-count" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/base64ai/latest/actions/scan-document-under-page-count', {
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
| `url` | string | yes | Public URL of the document to scan with a maximum page count. |
| `settings` | object | no | Scan settings object, for example {"maxPages":10}. Default: `{"maxPages":10}`. |

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
                  "rows": [
                    {
                      "cells": [
                        {
                          "confidence": 1,
                          "text": "string"
                        }
                      ],
                      "isHeader": true,
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
        "tables": [
          {}
        ]
      },
      "fields": {
        "benefitHeader": {
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
          "type": "string",
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
          "type": "string",
          "value": "string"
        },
        "embeddedFamilyDeductible": {
          "confidence": 1,
          "key": "string",
          "type": "string",
          "value": "string"
        },
        "familyDeductibleInNetworkProvider": {
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
        "familyDeductibleOutOfNetworkProvider": {
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
        "familyDrugDeductible": {
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
        "individualDeductibleInNetworkProvider": {
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
        "individualDeductibleOutOfNetworkProvider": {
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
        "individualDrugDeductible": {
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
        "isGated": {
          "confidence": 1,
          "key": "string",
          "type": "string",
          "value": "string"
        },
        "isHsaEligible": {
          "confidence": 1,
          "key": "string",
          "type": "string",
          "value": "string"
        },
        "moopFamilyDrugInNetworkProvider": {
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
        "moopFamilyDrugOutOfNetworkProvider": {
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
        "moopFamilyMedicalInNetworkProvider": {
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
        "moopFamilyMedicalOutOfNetworkProvider": {
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
        "moopIndividualDrugInNetworkProvider": {
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
        "moopIndividualDrugOutOfNetworkProvider": {
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
        "moopIndividualMedicalInNetworkProvider": {
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
        "moopIndividualMedicalOutOfNetworkProvider": {
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
        "needReferralToSeeASpecialist": {
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
        "notIncludedInTheOutOfPocketLimit": {
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
        "numberOfDeductibleTiers": {
          "confidence": 1,
          "key": "string",
          "value": 1
        },
        "numberOfMoopTiers": {
          "confidence": 1,
          "key": "string",
          "value": 1
        },
        "numberOfTiers": {
          "confidence": 1,
          "key": "string",
          "value": 1
        },
        "otherCoveredServicesAbortion": {
          "confidence": 1,
          "key": "string",
          "type": "string",
          "value": "string"
        },
        "otherCoveredServicesAcupuncture": {
          "confidence": 1,
          "key": "string",
          "type": "string",
          "value": "string"
        },
        "otherCoveredServicesAdultDental": {
          "confidence": 1,
          "key": "string",
          "type": "string",
          "value": "string"
        },
        "otherCoveredServicesBariatricSurgery": {
          "confidence": 1,
          "key": "string",
          "type": "string",
          "value": "string"
        },
        "otherCoveredServicesChiropracticServices": {
          "confidence": 1,
          "key": "string",
          "type": "string",
          "value": "string"
        },
        "otherCoveredServicesHearingAids": {
          "confidence": 1,
          "key": "string",
          "type": "string",
          "value": "string"
        },
        "otherCoveredServicesInfertilityTreatment": {
          "confidence": 1,
          "key": "string",
          "type": "string",
          "value": "string"
        },
        "otherCoveredServicesPrivateDutyNursing": {
          "confidence": 1,
          "key": "string",
          "type": "string",
          "value": "string"
        },
        "otherCoveredServicesRoutineEyeCare": {
          "confidence": 1,
          "key": "string",
          "type": "string",
          "value": "string"
        },
        "otherCoveredServicesWeightLossPrograms": {
          "confidence": 1,
          "key": "string",
          "type": "string",
          "value": "string"
        },
        "otherDeductibles": {
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
        "outOfPocketLimit": {
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
        "overallDeductible": {
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
        "payLessWithInNetworkProvider": {
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
        "planType": {
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
        },
        "servicesCoveredBeforeDeductible": {
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
        "servicesYouMayNeedBirthFacilityInNetworkProvider": {
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
        "servicesYouMayNeedBirthFacilityOutOfNetworkProvider": {
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
        "servicesYouMayNeedBirthOfficeVisitsInNetworkProvider": {
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
        "servicesYouMayNeedBirthOfficeVisitsOutOfNetworkProvider": {
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
        "servicesYouMayNeedBirthPhysicianInNetworkProvider": {
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
        "servicesYouMayNeedBirthPhysicianOutOfNetworkProvider": {
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
        "servicesYouMayNeedChildDentalCheckupInNetworkProvider": {
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
        "servicesYouMayNeedChildDentalCheckupOutOfNetworkProvider": {
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
        "servicesYouMayNeedChildEyeExamInNetworkProvider": {
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
        "servicesYouMayNeedChildEyeExamOutOfNetworkProvider": {
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
        "servicesYouMayNeedChildGlassesInNetworkProvider": {
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
        "servicesYouMayNeedChildGlassesOutOfNetworkProvider": {
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
        "servicesYouMayNeedDiagnosticTestInNetworkProvider": {
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
        "servicesYouMayNeedDiagnosticTestOutOfNetworkProvider": {
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
        "servicesYouMayNeedDrugFormularyUrl": {
          "confidence": 1,
          "key": "https://example.com",
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
          "value": "https://example.com"
        },
        "servicesYouMayNeedDurableMedicalEquipmentInNetworkProvider": {
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
        "servicesYouMayNeedDurableMedicalEquipmentOutOfNetworkProvider": {
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
        "servicesYouMayNeedEmergencyMedicalTransportationInNetworkProvider": {
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
        "servicesYouMayNeedEmergencyMedicalTransportationOutOfNetworkProvider": {
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
        "servicesYouMayNeedEmergencyRoomCareInNetworkProvider": {
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
        "servicesYouMayNeedEmergencyRoomCareOutOfNetworkProvider": {
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
        "servicesYouMayNeedGenericDrugsInNetworkProvider": {
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
        "servicesYouMayNeedGenericDrugsOutOfNetworkProvider": {
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
        "servicesYouMayNeedHabilitationServicesInNetworkProvider": {
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
        "servicesYouMayNeedHabilitationServicesOutOfNetworkProvider": {
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
        "servicesYouMayNeedHomeHealthcareInNetworkProvider": {
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
        "servicesYouMayNeedHomeHealthcareOutOfNetworkProvider": {
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
        "servicesYouMayNeedHospiceServicesInNetworkProvider": {
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
        "servicesYouMayNeedHospiceServicesOutOfNetworkProvider": {
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
        "servicesYouMayNeedHospitalStayFacilityFeeInNetworkProvider": {
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
        "servicesYouMayNeedHospitalStayFacilityFeeOutOfNetworkProvider": {
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
        "servicesYouMayNeedHospitalStayPhysicianFeeInNetworkProvider": {
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
        "servicesYouMayNeedHospitalStayPhysicianFeeOutOfNetworkProvider": {
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
        "servicesYouMayNeedImagingInNetworkProvider": {
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
        "servicesYouMayNeedImagingOutOfNetworkProvider": {
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
        "servicesYouMayNeedInpatientMentalServicesInNetworkProvider": {
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
        "servicesYouMayNeedInpatientMentalServicesOutOfNetworkProvider": {
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
        "servicesYouMayNeedMailOrderDrugCoefficient": {
          "confidence": 1,
          "key": "string",
          "type": "string",
          "value": 1
        },
        "servicesYouMayNeedNonPreferredBrandDrugsInNetworkProvider": {
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
        "servicesYouMayNeedNonPreferredBrandDrugsOutOfNetworkProvider": {
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
        "servicesYouMayNeedOutOfNetworkCoverage": {
          "confidence": 1,
          "key": "string",
          "type": "string",
          "value": "string"
        },
        "servicesYouMayNeedOutpatientFacilityFeeInNetworkProvider": {
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
        "servicesYouMayNeedOutpatientFacilityFeeOutOfNetworkProvider": {
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
        "servicesYouMayNeedOutpatientMentalServicesInNetworkProvider": {
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
        "servicesYouMayNeedOutpatientMentalServicesOutOfNetworkProvider": {
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
        "servicesYouMayNeedOutpatientPhysicianFeeInNetworkProvider": {
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
        "servicesYouMayNeedOutpatientPhysicianFeeOutOfNetworkProvider": {
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
        "servicesYouMayNeedPreferredBrandDrugsInNetworkProvider": {
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
        "servicesYouMayNeedPreferredBrandDrugsOutOfNetworkProvider": {
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
        "servicesYouMayNeedPreventiveCareInNetworkProvider": {
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
        "servicesYouMayNeedPreventiveCareOutOfNetworkProvider": {
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
        "servicesYouMayNeedPrimaryCareInNetworkProvider": {
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
        "servicesYouMayNeedPrimaryCareOutOfNetworkProvider": {
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
        "servicesYouMayNeedRehabilitationServicesInNetworkProvider": {
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
        "servicesYouMayNeedRehabilitationServicesOutOfNetworkProvider": {
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
        "servicesYouMayNeedSkilledNursingCareInNetworkProvider": {
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
        "servicesYouMayNeedSkilledNursingCareOutOfNetworkProvider": {
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
        "servicesYouMayNeedSpecialistVisitInNetworkProvider": {
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
        "servicesYouMayNeedSpecialistVisitOutOfNetworkProvider": {
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
        "servicesYouMayNeedSpecialtyDrugsInNetworkProvider": {
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
        "servicesYouMayNeedSpecialtyDrugsOutOfNetworkProvider": {
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
        "servicesYouMayNeedUrgentCareInNetworkProvider": {
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
        "servicesYouMayNeedUrgentCareOutOfNetworkProvider": {
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
| `features.dom.pages[].tables[].rows[].cells[].confidence` | number |  |
| `features.dom.pages[].tables[].rows[].cells[].text` | string |  |
| `features.dom.pages[].tables[].rows[].isHeader` | boolean |  |
| `features.dom.pages[].tables[].rows[].text` | string |  |
| `features.dom.pages[].tables[].text` | string |  |
| `features.dom.pages[].tables[].title` | string |  |
| `features.dom.pages[].text` | string |  |
| `features.dom.text` | string |  |
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
| `features.tables[]` | object |  |
| `fields.benefitHeader.confidence` | number |  |
| `fields.benefitHeader.key` | string |  |
| `fields.benefitHeader.location.bottomLeft.x` | number |  |
| `fields.benefitHeader.location.bottomLeft.y` | number |  |
| `fields.benefitHeader.location.bottomRight.x` | number |  |
| `fields.benefitHeader.location.bottomRight.y` | number |  |
| `fields.benefitHeader.location.pageNumber` | number |  |
| `fields.benefitHeader.location.topLeft.x` | number |  |
| `fields.benefitHeader.location.topLeft.y` | number |  |
| `fields.benefitHeader.location.topRight.x` | number |  |
| `fields.benefitHeader.location.topRight.y` | number |  |
| `fields.benefitHeader.value` | string |  |
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
| `fields.coverageEnd.type` | string |  |
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
| `fields.coverageStart.type` | string |  |
| `fields.coverageStart.value` | string |  |
| `fields.embeddedFamilyDeductible.confidence` | number |  |
| `fields.embeddedFamilyDeductible.key` | string |  |
| `fields.embeddedFamilyDeductible.type` | string |  |
| `fields.embeddedFamilyDeductible.value` | string |  |
| `fields.familyDeductibleInNetworkProvider.confidence` | number |  |
| `fields.familyDeductibleInNetworkProvider.key` | string |  |
| `fields.familyDeductibleInNetworkProvider.location.bottomLeft.x` | number |  |
| `fields.familyDeductibleInNetworkProvider.location.bottomLeft.y` | number |  |
| `fields.familyDeductibleInNetworkProvider.location.bottomRight.x` | number |  |
| `fields.familyDeductibleInNetworkProvider.location.bottomRight.y` | number |  |
| `fields.familyDeductibleInNetworkProvider.location.pageNumber` | number |  |
| `fields.familyDeductibleInNetworkProvider.location.topLeft.x` | number |  |
| `fields.familyDeductibleInNetworkProvider.location.topLeft.y` | number |  |
| `fields.familyDeductibleInNetworkProvider.location.topRight.x` | number |  |
| `fields.familyDeductibleInNetworkProvider.location.topRight.y` | number |  |
| `fields.familyDeductibleInNetworkProvider.value` | string |  |
| `fields.familyDeductibleOutOfNetworkProvider.confidence` | number |  |
| `fields.familyDeductibleOutOfNetworkProvider.key` | string |  |
| `fields.familyDeductibleOutOfNetworkProvider.location.bottomLeft.x` | number |  |
| `fields.familyDeductibleOutOfNetworkProvider.location.bottomLeft.y` | number |  |
| `fields.familyDeductibleOutOfNetworkProvider.location.bottomRight.x` | number |  |
| `fields.familyDeductibleOutOfNetworkProvider.location.bottomRight.y` | number |  |
| `fields.familyDeductibleOutOfNetworkProvider.location.pageNumber` | number |  |
| `fields.familyDeductibleOutOfNetworkProvider.location.topLeft.x` | number |  |
| `fields.familyDeductibleOutOfNetworkProvider.location.topLeft.y` | number |  |
| `fields.familyDeductibleOutOfNetworkProvider.location.topRight.x` | number |  |
| `fields.familyDeductibleOutOfNetworkProvider.location.topRight.y` | number |  |
| `fields.familyDeductibleOutOfNetworkProvider.value` | string |  |
| `fields.familyDrugDeductible.confidence` | number |  |
| `fields.familyDrugDeductible.key` | string |  |
| `fields.familyDrugDeductible.location.bottomLeft.x` | number |  |
| `fields.familyDrugDeductible.location.bottomLeft.y` | number |  |
| `fields.familyDrugDeductible.location.bottomRight.x` | number |  |
| `fields.familyDrugDeductible.location.bottomRight.y` | number |  |
| `fields.familyDrugDeductible.location.pageNumber` | number |  |
| `fields.familyDrugDeductible.location.topLeft.x` | number |  |
| `fields.familyDrugDeductible.location.topLeft.y` | number |  |
| `fields.familyDrugDeductible.location.topRight.x` | number |  |
| `fields.familyDrugDeductible.location.topRight.y` | number |  |
| `fields.familyDrugDeductible.value` | string |  |
| `fields.individualDeductibleInNetworkProvider.confidence` | number |  |
| `fields.individualDeductibleInNetworkProvider.key` | string |  |
| `fields.individualDeductibleInNetworkProvider.location.bottomLeft.x` | number |  |
| `fields.individualDeductibleInNetworkProvider.location.bottomLeft.y` | number |  |
| `fields.individualDeductibleInNetworkProvider.location.bottomRight.x` | number |  |
| `fields.individualDeductibleInNetworkProvider.location.bottomRight.y` | number |  |
| `fields.individualDeductibleInNetworkProvider.location.pageNumber` | number |  |
| `fields.individualDeductibleInNetworkProvider.location.topLeft.x` | number |  |
| `fields.individualDeductibleInNetworkProvider.location.topLeft.y` | number |  |
| `fields.individualDeductibleInNetworkProvider.location.topRight.x` | number |  |
| `fields.individualDeductibleInNetworkProvider.location.topRight.y` | number |  |
| `fields.individualDeductibleInNetworkProvider.value` | string |  |
| `fields.individualDeductibleOutOfNetworkProvider.confidence` | number |  |
| `fields.individualDeductibleOutOfNetworkProvider.key` | string |  |
| `fields.individualDeductibleOutOfNetworkProvider.location.bottomLeft.x` | number |  |
| `fields.individualDeductibleOutOfNetworkProvider.location.bottomLeft.y` | number |  |
| `fields.individualDeductibleOutOfNetworkProvider.location.bottomRight.x` | number |  |
| `fields.individualDeductibleOutOfNetworkProvider.location.bottomRight.y` | number |  |
| `fields.individualDeductibleOutOfNetworkProvider.location.pageNumber` | number |  |
| `fields.individualDeductibleOutOfNetworkProvider.location.topLeft.x` | number |  |
| `fields.individualDeductibleOutOfNetworkProvider.location.topLeft.y` | number |  |
| `fields.individualDeductibleOutOfNetworkProvider.location.topRight.x` | number |  |
| `fields.individualDeductibleOutOfNetworkProvider.location.topRight.y` | number |  |
| `fields.individualDeductibleOutOfNetworkProvider.value` | string |  |
| `fields.individualDrugDeductible.confidence` | number |  |
| `fields.individualDrugDeductible.key` | string |  |
| `fields.individualDrugDeductible.location.bottomLeft.x` | number |  |
| `fields.individualDrugDeductible.location.bottomLeft.y` | number |  |
| `fields.individualDrugDeductible.location.bottomRight.x` | number |  |
| `fields.individualDrugDeductible.location.bottomRight.y` | number |  |
| `fields.individualDrugDeductible.location.pageNumber` | number |  |
| `fields.individualDrugDeductible.location.topLeft.x` | number |  |
| `fields.individualDrugDeductible.location.topLeft.y` | number |  |
| `fields.individualDrugDeductible.location.topRight.x` | number |  |
| `fields.individualDrugDeductible.location.topRight.y` | number |  |
| `fields.individualDrugDeductible.value` | string |  |
| `fields.isGated.confidence` | number |  |
| `fields.isGated.key` | string |  |
| `fields.isGated.type` | string |  |
| `fields.isGated.value` | string |  |
| `fields.isHsaEligible.confidence` | number |  |
| `fields.isHsaEligible.key` | string |  |
| `fields.isHsaEligible.type` | string |  |
| `fields.isHsaEligible.value` | string |  |
| `fields.moopFamilyDrugInNetworkProvider.confidence` | number |  |
| `fields.moopFamilyDrugInNetworkProvider.key` | string |  |
| `fields.moopFamilyDrugInNetworkProvider.location.bottomLeft.x` | number |  |
| `fields.moopFamilyDrugInNetworkProvider.location.bottomLeft.y` | number |  |
| `fields.moopFamilyDrugInNetworkProvider.location.bottomRight.x` | number |  |
| `fields.moopFamilyDrugInNetworkProvider.location.bottomRight.y` | number |  |
| `fields.moopFamilyDrugInNetworkProvider.location.pageNumber` | number |  |
| `fields.moopFamilyDrugInNetworkProvider.location.topLeft.x` | number |  |
| `fields.moopFamilyDrugInNetworkProvider.location.topLeft.y` | number |  |
| `fields.moopFamilyDrugInNetworkProvider.location.topRight.x` | number |  |
| `fields.moopFamilyDrugInNetworkProvider.location.topRight.y` | number |  |
| `fields.moopFamilyDrugInNetworkProvider.value` | string |  |
| `fields.moopFamilyDrugOutOfNetworkProvider.confidence` | number |  |
| `fields.moopFamilyDrugOutOfNetworkProvider.key` | string |  |
| `fields.moopFamilyDrugOutOfNetworkProvider.location.bottomLeft.x` | number |  |
| `fields.moopFamilyDrugOutOfNetworkProvider.location.bottomLeft.y` | number |  |
| `fields.moopFamilyDrugOutOfNetworkProvider.location.bottomRight.x` | number |  |
| `fields.moopFamilyDrugOutOfNetworkProvider.location.bottomRight.y` | number |  |
| `fields.moopFamilyDrugOutOfNetworkProvider.location.pageNumber` | number |  |
| `fields.moopFamilyDrugOutOfNetworkProvider.location.topLeft.x` | number |  |
| `fields.moopFamilyDrugOutOfNetworkProvider.location.topLeft.y` | number |  |
| `fields.moopFamilyDrugOutOfNetworkProvider.location.topRight.x` | number |  |
| `fields.moopFamilyDrugOutOfNetworkProvider.location.topRight.y` | number |  |
| `fields.moopFamilyDrugOutOfNetworkProvider.value` | string |  |
| `fields.moopFamilyMedicalInNetworkProvider.confidence` | number |  |
| `fields.moopFamilyMedicalInNetworkProvider.key` | string |  |
| `fields.moopFamilyMedicalInNetworkProvider.location.bottomLeft.x` | number |  |
| `fields.moopFamilyMedicalInNetworkProvider.location.bottomLeft.y` | number |  |
| `fields.moopFamilyMedicalInNetworkProvider.location.bottomRight.x` | number |  |
| `fields.moopFamilyMedicalInNetworkProvider.location.bottomRight.y` | number |  |
| `fields.moopFamilyMedicalInNetworkProvider.location.pageNumber` | number |  |
| `fields.moopFamilyMedicalInNetworkProvider.location.topLeft.x` | number |  |
| `fields.moopFamilyMedicalInNetworkProvider.location.topLeft.y` | number |  |
| `fields.moopFamilyMedicalInNetworkProvider.location.topRight.x` | number |  |
| `fields.moopFamilyMedicalInNetworkProvider.location.topRight.y` | number |  |
| `fields.moopFamilyMedicalInNetworkProvider.value` | string |  |
| `fields.moopFamilyMedicalOutOfNetworkProvider.confidence` | number |  |
| `fields.moopFamilyMedicalOutOfNetworkProvider.key` | string |  |
| `fields.moopFamilyMedicalOutOfNetworkProvider.location.bottomLeft.x` | number |  |
| `fields.moopFamilyMedicalOutOfNetworkProvider.location.bottomLeft.y` | number |  |
| `fields.moopFamilyMedicalOutOfNetworkProvider.location.bottomRight.x` | number |  |
| `fields.moopFamilyMedicalOutOfNetworkProvider.location.bottomRight.y` | number |  |
| `fields.moopFamilyMedicalOutOfNetworkProvider.location.pageNumber` | number |  |
| `fields.moopFamilyMedicalOutOfNetworkProvider.location.topLeft.x` | number |  |
| `fields.moopFamilyMedicalOutOfNetworkProvider.location.topLeft.y` | number |  |
| `fields.moopFamilyMedicalOutOfNetworkProvider.location.topRight.x` | number |  |
| `fields.moopFamilyMedicalOutOfNetworkProvider.location.topRight.y` | number |  |
| `fields.moopFamilyMedicalOutOfNetworkProvider.value` | string |  |
| `fields.moopIndividualDrugInNetworkProvider.confidence` | number |  |
| `fields.moopIndividualDrugInNetworkProvider.key` | string |  |
| `fields.moopIndividualDrugInNetworkProvider.location.bottomLeft.x` | number |  |
| `fields.moopIndividualDrugInNetworkProvider.location.bottomLeft.y` | number |  |
| `fields.moopIndividualDrugInNetworkProvider.location.bottomRight.x` | number |  |
| `fields.moopIndividualDrugInNetworkProvider.location.bottomRight.y` | number |  |
| `fields.moopIndividualDrugInNetworkProvider.location.pageNumber` | number |  |
| `fields.moopIndividualDrugInNetworkProvider.location.topLeft.x` | number |  |
| `fields.moopIndividualDrugInNetworkProvider.location.topLeft.y` | number |  |
| `fields.moopIndividualDrugInNetworkProvider.location.topRight.x` | number |  |
| `fields.moopIndividualDrugInNetworkProvider.location.topRight.y` | number |  |
| `fields.moopIndividualDrugInNetworkProvider.value` | string |  |
| `fields.moopIndividualDrugOutOfNetworkProvider.confidence` | number |  |
| `fields.moopIndividualDrugOutOfNetworkProvider.key` | string |  |
| `fields.moopIndividualDrugOutOfNetworkProvider.location.bottomLeft.x` | number |  |
| `fields.moopIndividualDrugOutOfNetworkProvider.location.bottomLeft.y` | number |  |
| `fields.moopIndividualDrugOutOfNetworkProvider.location.bottomRight.x` | number |  |
| `fields.moopIndividualDrugOutOfNetworkProvider.location.bottomRight.y` | number |  |
| `fields.moopIndividualDrugOutOfNetworkProvider.location.pageNumber` | number |  |
| `fields.moopIndividualDrugOutOfNetworkProvider.location.topLeft.x` | number |  |
| `fields.moopIndividualDrugOutOfNetworkProvider.location.topLeft.y` | number |  |
| `fields.moopIndividualDrugOutOfNetworkProvider.location.topRight.x` | number |  |
| `fields.moopIndividualDrugOutOfNetworkProvider.location.topRight.y` | number |  |
| `fields.moopIndividualDrugOutOfNetworkProvider.value` | string |  |
| `fields.moopIndividualMedicalInNetworkProvider.confidence` | number |  |
| `fields.moopIndividualMedicalInNetworkProvider.key` | string |  |
| `fields.moopIndividualMedicalInNetworkProvider.location.bottomLeft.x` | number |  |
| `fields.moopIndividualMedicalInNetworkProvider.location.bottomLeft.y` | number |  |
| `fields.moopIndividualMedicalInNetworkProvider.location.bottomRight.x` | number |  |
| `fields.moopIndividualMedicalInNetworkProvider.location.bottomRight.y` | number |  |
| `fields.moopIndividualMedicalInNetworkProvider.location.pageNumber` | number |  |
| `fields.moopIndividualMedicalInNetworkProvider.location.topLeft.x` | number |  |
| `fields.moopIndividualMedicalInNetworkProvider.location.topLeft.y` | number |  |
| `fields.moopIndividualMedicalInNetworkProvider.location.topRight.x` | number |  |
| `fields.moopIndividualMedicalInNetworkProvider.location.topRight.y` | number |  |
| `fields.moopIndividualMedicalInNetworkProvider.value` | string |  |
| `fields.moopIndividualMedicalOutOfNetworkProvider.confidence` | number |  |
| `fields.moopIndividualMedicalOutOfNetworkProvider.key` | string |  |
| `fields.moopIndividualMedicalOutOfNetworkProvider.location.bottomLeft.x` | number |  |
| `fields.moopIndividualMedicalOutOfNetworkProvider.location.bottomLeft.y` | number |  |
| `fields.moopIndividualMedicalOutOfNetworkProvider.location.bottomRight.x` | number |  |
| `fields.moopIndividualMedicalOutOfNetworkProvider.location.bottomRight.y` | number |  |
| `fields.moopIndividualMedicalOutOfNetworkProvider.location.pageNumber` | number |  |
| `fields.moopIndividualMedicalOutOfNetworkProvider.location.topLeft.x` | number |  |
| `fields.moopIndividualMedicalOutOfNetworkProvider.location.topLeft.y` | number |  |
| `fields.moopIndividualMedicalOutOfNetworkProvider.location.topRight.x` | number |  |
| `fields.moopIndividualMedicalOutOfNetworkProvider.location.topRight.y` | number |  |
| `fields.moopIndividualMedicalOutOfNetworkProvider.value` | string |  |
| `fields.needReferralToSeeASpecialist.confidence` | number |  |
| `fields.needReferralToSeeASpecialist.key` | string |  |
| `fields.needReferralToSeeASpecialist.location.bottomLeft.x` | number |  |
| `fields.needReferralToSeeASpecialist.location.bottomLeft.y` | number |  |
| `fields.needReferralToSeeASpecialist.location.bottomRight.x` | number |  |
| `fields.needReferralToSeeASpecialist.location.bottomRight.y` | number |  |
| `fields.needReferralToSeeASpecialist.location.pageNumber` | number |  |
| `fields.needReferralToSeeASpecialist.location.topLeft.x` | number |  |
| `fields.needReferralToSeeASpecialist.location.topLeft.y` | number |  |
| `fields.needReferralToSeeASpecialist.location.topRight.x` | number |  |
| `fields.needReferralToSeeASpecialist.location.topRight.y` | number |  |
| `fields.needReferralToSeeASpecialist.value` | string |  |
| `fields.notIncludedInTheOutOfPocketLimit.confidence` | number |  |
| `fields.notIncludedInTheOutOfPocketLimit.key` | string |  |
| `fields.notIncludedInTheOutOfPocketLimit.location.bottomLeft.x` | number |  |
| `fields.notIncludedInTheOutOfPocketLimit.location.bottomLeft.y` | number |  |
| `fields.notIncludedInTheOutOfPocketLimit.location.bottomRight.x` | number |  |
| `fields.notIncludedInTheOutOfPocketLimit.location.bottomRight.y` | number |  |
| `fields.notIncludedInTheOutOfPocketLimit.location.pageNumber` | number |  |
| `fields.notIncludedInTheOutOfPocketLimit.location.topLeft.x` | number |  |
| `fields.notIncludedInTheOutOfPocketLimit.location.topLeft.y` | number |  |
| `fields.notIncludedInTheOutOfPocketLimit.location.topRight.x` | number |  |
| `fields.notIncludedInTheOutOfPocketLimit.location.topRight.y` | number |  |
| `fields.notIncludedInTheOutOfPocketLimit.value` | string |  |
| `fields.numberOfDeductibleTiers.confidence` | number |  |
| `fields.numberOfDeductibleTiers.key` | string |  |
| `fields.numberOfDeductibleTiers.value` | number |  |
| `fields.numberOfMoopTiers.confidence` | number |  |
| `fields.numberOfMoopTiers.key` | string |  |
| `fields.numberOfMoopTiers.value` | number |  |
| `fields.numberOfTiers.confidence` | number |  |
| `fields.numberOfTiers.key` | string |  |
| `fields.numberOfTiers.value` | number |  |
| `fields.otherCoveredServicesAbortion.confidence` | number |  |
| `fields.otherCoveredServicesAbortion.key` | string |  |
| `fields.otherCoveredServicesAbortion.type` | string |  |
| `fields.otherCoveredServicesAbortion.value` | string |  |
| `fields.otherCoveredServicesAcupuncture.confidence` | number |  |
| `fields.otherCoveredServicesAcupuncture.key` | string |  |
| `fields.otherCoveredServicesAcupuncture.type` | string |  |
| `fields.otherCoveredServicesAcupuncture.value` | string |  |
| `fields.otherCoveredServicesAdultDental.confidence` | number |  |
| `fields.otherCoveredServicesAdultDental.key` | string |  |
| `fields.otherCoveredServicesAdultDental.type` | string |  |
| `fields.otherCoveredServicesAdultDental.value` | string |  |
| `fields.otherCoveredServicesBariatricSurgery.confidence` | number |  |
| `fields.otherCoveredServicesBariatricSurgery.key` | string |  |
| `fields.otherCoveredServicesBariatricSurgery.type` | string |  |
| `fields.otherCoveredServicesBariatricSurgery.value` | string |  |
| `fields.otherCoveredServicesChiropracticServices.confidence` | number |  |
| `fields.otherCoveredServicesChiropracticServices.key` | string |  |
| `fields.otherCoveredServicesChiropracticServices.type` | string |  |
| `fields.otherCoveredServicesChiropracticServices.value` | string |  |
| `fields.otherCoveredServicesHearingAids.confidence` | number |  |
| `fields.otherCoveredServicesHearingAids.key` | string |  |
| `fields.otherCoveredServicesHearingAids.type` | string |  |
| `fields.otherCoveredServicesHearingAids.value` | string |  |
| `fields.otherCoveredServicesInfertilityTreatment.confidence` | number |  |
| `fields.otherCoveredServicesInfertilityTreatment.key` | string |  |
| `fields.otherCoveredServicesInfertilityTreatment.type` | string |  |
| `fields.otherCoveredServicesInfertilityTreatment.value` | string |  |
| `fields.otherCoveredServicesPrivateDutyNursing.confidence` | number |  |
| `fields.otherCoveredServicesPrivateDutyNursing.key` | string |  |
| `fields.otherCoveredServicesPrivateDutyNursing.type` | string |  |
| `fields.otherCoveredServicesPrivateDutyNursing.value` | string |  |
| `fields.otherCoveredServicesRoutineEyeCare.confidence` | number |  |
| `fields.otherCoveredServicesRoutineEyeCare.key` | string |  |
| `fields.otherCoveredServicesRoutineEyeCare.type` | string |  |
| `fields.otherCoveredServicesRoutineEyeCare.value` | string |  |
| `fields.otherCoveredServicesWeightLossPrograms.confidence` | number |  |
| `fields.otherCoveredServicesWeightLossPrograms.key` | string |  |
| `fields.otherCoveredServicesWeightLossPrograms.type` | string |  |
| `fields.otherCoveredServicesWeightLossPrograms.value` | string |  |
| `fields.otherDeductibles.confidence` | number |  |
| `fields.otherDeductibles.key` | string |  |
| `fields.otherDeductibles.location.bottomLeft.x` | number |  |
| `fields.otherDeductibles.location.bottomLeft.y` | number |  |
| `fields.otherDeductibles.location.bottomRight.x` | number |  |
| `fields.otherDeductibles.location.bottomRight.y` | number |  |
| `fields.otherDeductibles.location.pageNumber` | number |  |
| `fields.otherDeductibles.location.topLeft.x` | number |  |
| `fields.otherDeductibles.location.topLeft.y` | number |  |
| `fields.otherDeductibles.location.topRight.x` | number |  |
| `fields.otherDeductibles.location.topRight.y` | number |  |
| `fields.otherDeductibles.value` | string |  |
| `fields.outOfPocketLimit.confidence` | number |  |
| `fields.outOfPocketLimit.key` | string |  |
| `fields.outOfPocketLimit.location.bottomLeft.x` | number |  |
| `fields.outOfPocketLimit.location.bottomLeft.y` | number |  |
| `fields.outOfPocketLimit.location.bottomRight.x` | number |  |
| `fields.outOfPocketLimit.location.bottomRight.y` | number |  |
| `fields.outOfPocketLimit.location.pageNumber` | number |  |
| `fields.outOfPocketLimit.location.topLeft.x` | number |  |
| `fields.outOfPocketLimit.location.topLeft.y` | number |  |
| `fields.outOfPocketLimit.location.topRight.x` | number |  |
| `fields.outOfPocketLimit.location.topRight.y` | number |  |
| `fields.outOfPocketLimit.value` | string |  |
| `fields.overallDeductible.confidence` | number |  |
| `fields.overallDeductible.key` | string |  |
| `fields.overallDeductible.location.bottomLeft.x` | number |  |
| `fields.overallDeductible.location.bottomLeft.y` | number |  |
| `fields.overallDeductible.location.bottomRight.x` | number |  |
| `fields.overallDeductible.location.bottomRight.y` | number |  |
| `fields.overallDeductible.location.pageNumber` | number |  |
| `fields.overallDeductible.location.topLeft.x` | number |  |
| `fields.overallDeductible.location.topLeft.y` | number |  |
| `fields.overallDeductible.location.topRight.x` | number |  |
| `fields.overallDeductible.location.topRight.y` | number |  |
| `fields.overallDeductible.value` | string |  |
| `fields.payLessWithInNetworkProvider.confidence` | number |  |
| `fields.payLessWithInNetworkProvider.key` | string |  |
| `fields.payLessWithInNetworkProvider.location.bottomLeft.x` | number |  |
| `fields.payLessWithInNetworkProvider.location.bottomLeft.y` | number |  |
| `fields.payLessWithInNetworkProvider.location.bottomRight.x` | number |  |
| `fields.payLessWithInNetworkProvider.location.bottomRight.y` | number |  |
| `fields.payLessWithInNetworkProvider.location.pageNumber` | number |  |
| `fields.payLessWithInNetworkProvider.location.topLeft.x` | number |  |
| `fields.payLessWithInNetworkProvider.location.topLeft.y` | number |  |
| `fields.payLessWithInNetworkProvider.location.topRight.x` | number |  |
| `fields.payLessWithInNetworkProvider.location.topRight.y` | number |  |
| `fields.payLessWithInNetworkProvider.type` | string |  |
| `fields.payLessWithInNetworkProvider.value` | string |  |
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
| `fields.planType.confidence` | number |  |
| `fields.planType.key` | string |  |
| `fields.planType.location.bottomLeft.x` | number |  |
| `fields.planType.location.bottomLeft.y` | number |  |
| `fields.planType.location.bottomRight.x` | number |  |
| `fields.planType.location.bottomRight.y` | number |  |
| `fields.planType.location.pageNumber` | number |  |
| `fields.planType.location.topLeft.x` | number |  |
| `fields.planType.location.topLeft.y` | number |  |
| `fields.planType.location.topRight.x` | number |  |
| `fields.planType.location.topRight.y` | number |  |
| `fields.planType.value` | string |  |
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
| `fields.servicesCoveredBeforeDeductible.confidence` | number |  |
| `fields.servicesCoveredBeforeDeductible.key` | string |  |
| `fields.servicesCoveredBeforeDeductible.location.bottomLeft.x` | number |  |
| `fields.servicesCoveredBeforeDeductible.location.bottomLeft.y` | number |  |
| `fields.servicesCoveredBeforeDeductible.location.bottomRight.x` | number |  |
| `fields.servicesCoveredBeforeDeductible.location.bottomRight.y` | number |  |
| `fields.servicesCoveredBeforeDeductible.location.pageNumber` | number |  |
| `fields.servicesCoveredBeforeDeductible.location.topLeft.x` | number |  |
| `fields.servicesCoveredBeforeDeductible.location.topLeft.y` | number |  |
| `fields.servicesCoveredBeforeDeductible.location.topRight.x` | number |  |
| `fields.servicesCoveredBeforeDeductible.location.topRight.y` | number |  |
| `fields.servicesCoveredBeforeDeductible.value` | string |  |
| `fields.servicesYouMayNeedBirthFacilityInNetworkProvider.confidence` | number |  |
| `fields.servicesYouMayNeedBirthFacilityInNetworkProvider.key` | string |  |
| `fields.servicesYouMayNeedBirthFacilityInNetworkProvider.location.bottomLeft.x` | number |  |
| `fields.servicesYouMayNeedBirthFacilityInNetworkProvider.location.bottomLeft.y` | number |  |
| `fields.servicesYouMayNeedBirthFacilityInNetworkProvider.location.bottomRight.x` | number |  |
| `fields.servicesYouMayNeedBirthFacilityInNetworkProvider.location.bottomRight.y` | number |  |
| `fields.servicesYouMayNeedBirthFacilityInNetworkProvider.location.pageNumber` | number |  |
| `fields.servicesYouMayNeedBirthFacilityInNetworkProvider.location.topLeft.x` | number |  |
| `fields.servicesYouMayNeedBirthFacilityInNetworkProvider.location.topLeft.y` | number |  |
| `fields.servicesYouMayNeedBirthFacilityInNetworkProvider.location.topRight.x` | number |  |
| `fields.servicesYouMayNeedBirthFacilityInNetworkProvider.location.topRight.y` | number |  |
| `fields.servicesYouMayNeedBirthFacilityInNetworkProvider.type` | string |  |
| `fields.servicesYouMayNeedBirthFacilityInNetworkProvider.value` | string |  |
| `fields.servicesYouMayNeedBirthFacilityOutOfNetworkProvider.confidence` | number |  |
| `fields.servicesYouMayNeedBirthFacilityOutOfNetworkProvider.key` | string |  |
| `fields.servicesYouMayNeedBirthFacilityOutOfNetworkProvider.location.bottomLeft.x` | number |  |
| `fields.servicesYouMayNeedBirthFacilityOutOfNetworkProvider.location.bottomLeft.y` | number |  |
| `fields.servicesYouMayNeedBirthFacilityOutOfNetworkProvider.location.bottomRight.x` | number |  |
| `fields.servicesYouMayNeedBirthFacilityOutOfNetworkProvider.location.bottomRight.y` | number |  |
| `fields.servicesYouMayNeedBirthFacilityOutOfNetworkProvider.location.pageNumber` | number |  |
| `fields.servicesYouMayNeedBirthFacilityOutOfNetworkProvider.location.topLeft.x` | number |  |
| `fields.servicesYouMayNeedBirthFacilityOutOfNetworkProvider.location.topLeft.y` | number |  |
| `fields.servicesYouMayNeedBirthFacilityOutOfNetworkProvider.location.topRight.x` | number |  |
| `fields.servicesYouMayNeedBirthFacilityOutOfNetworkProvider.location.topRight.y` | number |  |
| `fields.servicesYouMayNeedBirthFacilityOutOfNetworkProvider.type` | string |  |
| `fields.servicesYouMayNeedBirthFacilityOutOfNetworkProvider.value` | string |  |
| `fields.servicesYouMayNeedBirthOfficeVisitsInNetworkProvider.confidence` | number |  |
| `fields.servicesYouMayNeedBirthOfficeVisitsInNetworkProvider.key` | string |  |
| `fields.servicesYouMayNeedBirthOfficeVisitsInNetworkProvider.location.bottomLeft.x` | number |  |
| `fields.servicesYouMayNeedBirthOfficeVisitsInNetworkProvider.location.bottomLeft.y` | number |  |
| `fields.servicesYouMayNeedBirthOfficeVisitsInNetworkProvider.location.bottomRight.x` | number |  |
| `fields.servicesYouMayNeedBirthOfficeVisitsInNetworkProvider.location.bottomRight.y` | number |  |
| `fields.servicesYouMayNeedBirthOfficeVisitsInNetworkProvider.location.pageNumber` | number |  |
| `fields.servicesYouMayNeedBirthOfficeVisitsInNetworkProvider.location.topLeft.x` | number |  |
| `fields.servicesYouMayNeedBirthOfficeVisitsInNetworkProvider.location.topLeft.y` | number |  |
| `fields.servicesYouMayNeedBirthOfficeVisitsInNetworkProvider.location.topRight.x` | number |  |
| `fields.servicesYouMayNeedBirthOfficeVisitsInNetworkProvider.location.topRight.y` | number |  |
| `fields.servicesYouMayNeedBirthOfficeVisitsInNetworkProvider.type` | string |  |
| `fields.servicesYouMayNeedBirthOfficeVisitsInNetworkProvider.value` | string |  |
| `fields.servicesYouMayNeedBirthOfficeVisitsOutOfNetworkProvider.confidence` | number |  |
| `fields.servicesYouMayNeedBirthOfficeVisitsOutOfNetworkProvider.key` | string |  |
| `fields.servicesYouMayNeedBirthOfficeVisitsOutOfNetworkProvider.location.bottomLeft.x` | number |  |
| `fields.servicesYouMayNeedBirthOfficeVisitsOutOfNetworkProvider.location.bottomLeft.y` | number |  |
| `fields.servicesYouMayNeedBirthOfficeVisitsOutOfNetworkProvider.location.bottomRight.x` | number |  |
| `fields.servicesYouMayNeedBirthOfficeVisitsOutOfNetworkProvider.location.bottomRight.y` | number |  |
| `fields.servicesYouMayNeedBirthOfficeVisitsOutOfNetworkProvider.location.pageNumber` | number |  |
| `fields.servicesYouMayNeedBirthOfficeVisitsOutOfNetworkProvider.location.topLeft.x` | number |  |
| `fields.servicesYouMayNeedBirthOfficeVisitsOutOfNetworkProvider.location.topLeft.y` | number |  |
| `fields.servicesYouMayNeedBirthOfficeVisitsOutOfNetworkProvider.location.topRight.x` | number |  |
| `fields.servicesYouMayNeedBirthOfficeVisitsOutOfNetworkProvider.location.topRight.y` | number |  |
| `fields.servicesYouMayNeedBirthOfficeVisitsOutOfNetworkProvider.type` | string |  |
| `fields.servicesYouMayNeedBirthOfficeVisitsOutOfNetworkProvider.value` | string |  |
| `fields.servicesYouMayNeedBirthPhysicianInNetworkProvider.confidence` | number |  |
| `fields.servicesYouMayNeedBirthPhysicianInNetworkProvider.key` | string |  |
| `fields.servicesYouMayNeedBirthPhysicianInNetworkProvider.location.bottomLeft.x` | number |  |
| `fields.servicesYouMayNeedBirthPhysicianInNetworkProvider.location.bottomLeft.y` | number |  |
| `fields.servicesYouMayNeedBirthPhysicianInNetworkProvider.location.bottomRight.x` | number |  |
| `fields.servicesYouMayNeedBirthPhysicianInNetworkProvider.location.bottomRight.y` | number |  |
| `fields.servicesYouMayNeedBirthPhysicianInNetworkProvider.location.pageNumber` | number |  |
| `fields.servicesYouMayNeedBirthPhysicianInNetworkProvider.location.topLeft.x` | number |  |
| `fields.servicesYouMayNeedBirthPhysicianInNetworkProvider.location.topLeft.y` | number |  |
| `fields.servicesYouMayNeedBirthPhysicianInNetworkProvider.location.topRight.x` | number |  |
| `fields.servicesYouMayNeedBirthPhysicianInNetworkProvider.location.topRight.y` | number |  |
| `fields.servicesYouMayNeedBirthPhysicianInNetworkProvider.type` | string |  |
| `fields.servicesYouMayNeedBirthPhysicianInNetworkProvider.value` | string |  |
| `fields.servicesYouMayNeedBirthPhysicianOutOfNetworkProvider.confidence` | number |  |
| `fields.servicesYouMayNeedBirthPhysicianOutOfNetworkProvider.key` | string |  |
| `fields.servicesYouMayNeedBirthPhysicianOutOfNetworkProvider.location.bottomLeft.x` | number |  |
| `fields.servicesYouMayNeedBirthPhysicianOutOfNetworkProvider.location.bottomLeft.y` | number |  |
| `fields.servicesYouMayNeedBirthPhysicianOutOfNetworkProvider.location.bottomRight.x` | number |  |
| `fields.servicesYouMayNeedBirthPhysicianOutOfNetworkProvider.location.bottomRight.y` | number |  |
| `fields.servicesYouMayNeedBirthPhysicianOutOfNetworkProvider.location.pageNumber` | number |  |
| `fields.servicesYouMayNeedBirthPhysicianOutOfNetworkProvider.location.topLeft.x` | number |  |
| `fields.servicesYouMayNeedBirthPhysicianOutOfNetworkProvider.location.topLeft.y` | number |  |
| `fields.servicesYouMayNeedBirthPhysicianOutOfNetworkProvider.location.topRight.x` | number |  |
| `fields.servicesYouMayNeedBirthPhysicianOutOfNetworkProvider.location.topRight.y` | number |  |
| `fields.servicesYouMayNeedBirthPhysicianOutOfNetworkProvider.type` | string |  |
| `fields.servicesYouMayNeedBirthPhysicianOutOfNetworkProvider.value` | string |  |
| `fields.servicesYouMayNeedChildDentalCheckupInNetworkProvider.confidence` | number |  |
| `fields.servicesYouMayNeedChildDentalCheckupInNetworkProvider.key` | string |  |
| `fields.servicesYouMayNeedChildDentalCheckupInNetworkProvider.location.bottomLeft.x` | number |  |
| `fields.servicesYouMayNeedChildDentalCheckupInNetworkProvider.location.bottomLeft.y` | number |  |
| `fields.servicesYouMayNeedChildDentalCheckupInNetworkProvider.location.bottomRight.x` | number |  |
| `fields.servicesYouMayNeedChildDentalCheckupInNetworkProvider.location.bottomRight.y` | number |  |
| `fields.servicesYouMayNeedChildDentalCheckupInNetworkProvider.location.pageNumber` | number |  |
| `fields.servicesYouMayNeedChildDentalCheckupInNetworkProvider.location.topLeft.x` | number |  |
| `fields.servicesYouMayNeedChildDentalCheckupInNetworkProvider.location.topLeft.y` | number |  |
| `fields.servicesYouMayNeedChildDentalCheckupInNetworkProvider.location.topRight.x` | number |  |
| `fields.servicesYouMayNeedChildDentalCheckupInNetworkProvider.location.topRight.y` | number |  |
| `fields.servicesYouMayNeedChildDentalCheckupInNetworkProvider.type` | string |  |
| `fields.servicesYouMayNeedChildDentalCheckupInNetworkProvider.value` | string |  |
| `fields.servicesYouMayNeedChildDentalCheckupOutOfNetworkProvider.confidence` | number |  |
| `fields.servicesYouMayNeedChildDentalCheckupOutOfNetworkProvider.key` | string |  |
| `fields.servicesYouMayNeedChildDentalCheckupOutOfNetworkProvider.location.bottomLeft.x` | number |  |
| `fields.servicesYouMayNeedChildDentalCheckupOutOfNetworkProvider.location.bottomLeft.y` | number |  |
| `fields.servicesYouMayNeedChildDentalCheckupOutOfNetworkProvider.location.bottomRight.x` | number |  |
| `fields.servicesYouMayNeedChildDentalCheckupOutOfNetworkProvider.location.bottomRight.y` | number |  |
| `fields.servicesYouMayNeedChildDentalCheckupOutOfNetworkProvider.location.pageNumber` | number |  |
| `fields.servicesYouMayNeedChildDentalCheckupOutOfNetworkProvider.location.topLeft.x` | number |  |
| `fields.servicesYouMayNeedChildDentalCheckupOutOfNetworkProvider.location.topLeft.y` | number |  |
| `fields.servicesYouMayNeedChildDentalCheckupOutOfNetworkProvider.location.topRight.x` | number |  |
| `fields.servicesYouMayNeedChildDentalCheckupOutOfNetworkProvider.location.topRight.y` | number |  |
| `fields.servicesYouMayNeedChildDentalCheckupOutOfNetworkProvider.type` | string |  |
| `fields.servicesYouMayNeedChildDentalCheckupOutOfNetworkProvider.value` | string |  |
| `fields.servicesYouMayNeedChildEyeExamInNetworkProvider.confidence` | number |  |
| `fields.servicesYouMayNeedChildEyeExamInNetworkProvider.key` | string |  |
| `fields.servicesYouMayNeedChildEyeExamInNetworkProvider.location.bottomLeft.x` | number |  |
| `fields.servicesYouMayNeedChildEyeExamInNetworkProvider.location.bottomLeft.y` | number |  |
| `fields.servicesYouMayNeedChildEyeExamInNetworkProvider.location.bottomRight.x` | number |  |
| `fields.servicesYouMayNeedChildEyeExamInNetworkProvider.location.bottomRight.y` | number |  |
| `fields.servicesYouMayNeedChildEyeExamInNetworkProvider.location.pageNumber` | number |  |
| `fields.servicesYouMayNeedChildEyeExamInNetworkProvider.location.topLeft.x` | number |  |
| `fields.servicesYouMayNeedChildEyeExamInNetworkProvider.location.topLeft.y` | number |  |
| `fields.servicesYouMayNeedChildEyeExamInNetworkProvider.location.topRight.x` | number |  |
| `fields.servicesYouMayNeedChildEyeExamInNetworkProvider.location.topRight.y` | number |  |
| `fields.servicesYouMayNeedChildEyeExamInNetworkProvider.type` | string |  |
| `fields.servicesYouMayNeedChildEyeExamInNetworkProvider.value` | string |  |
| `fields.servicesYouMayNeedChildEyeExamOutOfNetworkProvider.confidence` | number |  |
| `fields.servicesYouMayNeedChildEyeExamOutOfNetworkProvider.key` | string |  |
| `fields.servicesYouMayNeedChildEyeExamOutOfNetworkProvider.location.bottomLeft.x` | number |  |
| `fields.servicesYouMayNeedChildEyeExamOutOfNetworkProvider.location.bottomLeft.y` | number |  |
| `fields.servicesYouMayNeedChildEyeExamOutOfNetworkProvider.location.bottomRight.x` | number |  |
| `fields.servicesYouMayNeedChildEyeExamOutOfNetworkProvider.location.bottomRight.y` | number |  |
| `fields.servicesYouMayNeedChildEyeExamOutOfNetworkProvider.location.pageNumber` | number |  |
| `fields.servicesYouMayNeedChildEyeExamOutOfNetworkProvider.location.topLeft.x` | number |  |
| `fields.servicesYouMayNeedChildEyeExamOutOfNetworkProvider.location.topLeft.y` | number |  |
| `fields.servicesYouMayNeedChildEyeExamOutOfNetworkProvider.location.topRight.x` | number |  |
| `fields.servicesYouMayNeedChildEyeExamOutOfNetworkProvider.location.topRight.y` | number |  |
| `fields.servicesYouMayNeedChildEyeExamOutOfNetworkProvider.type` | string |  |
| `fields.servicesYouMayNeedChildEyeExamOutOfNetworkProvider.value` | string |  |
| `fields.servicesYouMayNeedChildGlassesInNetworkProvider.confidence` | number |  |
| `fields.servicesYouMayNeedChildGlassesInNetworkProvider.key` | string |  |
| `fields.servicesYouMayNeedChildGlassesInNetworkProvider.location.bottomLeft.x` | number |  |
| `fields.servicesYouMayNeedChildGlassesInNetworkProvider.location.bottomLeft.y` | number |  |
| `fields.servicesYouMayNeedChildGlassesInNetworkProvider.location.bottomRight.x` | number |  |
| `fields.servicesYouMayNeedChildGlassesInNetworkProvider.location.bottomRight.y` | number |  |
| `fields.servicesYouMayNeedChildGlassesInNetworkProvider.location.pageNumber` | number |  |
| `fields.servicesYouMayNeedChildGlassesInNetworkProvider.location.topLeft.x` | number |  |
| `fields.servicesYouMayNeedChildGlassesInNetworkProvider.location.topLeft.y` | number |  |
| `fields.servicesYouMayNeedChildGlassesInNetworkProvider.location.topRight.x` | number |  |
| `fields.servicesYouMayNeedChildGlassesInNetworkProvider.location.topRight.y` | number |  |
| `fields.servicesYouMayNeedChildGlassesInNetworkProvider.type` | string |  |
| `fields.servicesYouMayNeedChildGlassesInNetworkProvider.value` | string |  |
| `fields.servicesYouMayNeedChildGlassesOutOfNetworkProvider.confidence` | number |  |
| `fields.servicesYouMayNeedChildGlassesOutOfNetworkProvider.key` | string |  |
| `fields.servicesYouMayNeedChildGlassesOutOfNetworkProvider.location.bottomLeft.x` | number |  |
| `fields.servicesYouMayNeedChildGlassesOutOfNetworkProvider.location.bottomLeft.y` | number |  |
| `fields.servicesYouMayNeedChildGlassesOutOfNetworkProvider.location.bottomRight.x` | number |  |
| `fields.servicesYouMayNeedChildGlassesOutOfNetworkProvider.location.bottomRight.y` | number |  |
| `fields.servicesYouMayNeedChildGlassesOutOfNetworkProvider.location.pageNumber` | number |  |
| `fields.servicesYouMayNeedChildGlassesOutOfNetworkProvider.location.topLeft.x` | number |  |
| `fields.servicesYouMayNeedChildGlassesOutOfNetworkProvider.location.topLeft.y` | number |  |
| `fields.servicesYouMayNeedChildGlassesOutOfNetworkProvider.location.topRight.x` | number |  |
| `fields.servicesYouMayNeedChildGlassesOutOfNetworkProvider.location.topRight.y` | number |  |
| `fields.servicesYouMayNeedChildGlassesOutOfNetworkProvider.type` | string |  |
| `fields.servicesYouMayNeedChildGlassesOutOfNetworkProvider.value` | string |  |
| `fields.servicesYouMayNeedDiagnosticTestInNetworkProvider.confidence` | number |  |
| `fields.servicesYouMayNeedDiagnosticTestInNetworkProvider.key` | string |  |
| `fields.servicesYouMayNeedDiagnosticTestInNetworkProvider.location.bottomLeft.x` | number |  |
| `fields.servicesYouMayNeedDiagnosticTestInNetworkProvider.location.bottomLeft.y` | number |  |
| `fields.servicesYouMayNeedDiagnosticTestInNetworkProvider.location.bottomRight.x` | number |  |
| `fields.servicesYouMayNeedDiagnosticTestInNetworkProvider.location.bottomRight.y` | number |  |
| `fields.servicesYouMayNeedDiagnosticTestInNetworkProvider.location.pageNumber` | number |  |
| `fields.servicesYouMayNeedDiagnosticTestInNetworkProvider.location.topLeft.x` | number |  |
| `fields.servicesYouMayNeedDiagnosticTestInNetworkProvider.location.topLeft.y` | number |  |
| `fields.servicesYouMayNeedDiagnosticTestInNetworkProvider.location.topRight.x` | number |  |
| `fields.servicesYouMayNeedDiagnosticTestInNetworkProvider.location.topRight.y` | number |  |
| `fields.servicesYouMayNeedDiagnosticTestInNetworkProvider.type` | string |  |
| `fields.servicesYouMayNeedDiagnosticTestInNetworkProvider.value` | string |  |
| `fields.servicesYouMayNeedDiagnosticTestOutOfNetworkProvider.confidence` | number |  |
| `fields.servicesYouMayNeedDiagnosticTestOutOfNetworkProvider.key` | string |  |
| `fields.servicesYouMayNeedDiagnosticTestOutOfNetworkProvider.location.bottomLeft.x` | number |  |
| `fields.servicesYouMayNeedDiagnosticTestOutOfNetworkProvider.location.bottomLeft.y` | number |  |
| `fields.servicesYouMayNeedDiagnosticTestOutOfNetworkProvider.location.bottomRight.x` | number |  |
| `fields.servicesYouMayNeedDiagnosticTestOutOfNetworkProvider.location.bottomRight.y` | number |  |
| `fields.servicesYouMayNeedDiagnosticTestOutOfNetworkProvider.location.pageNumber` | number |  |
| `fields.servicesYouMayNeedDiagnosticTestOutOfNetworkProvider.location.topLeft.x` | number |  |
| `fields.servicesYouMayNeedDiagnosticTestOutOfNetworkProvider.location.topLeft.y` | number |  |
| `fields.servicesYouMayNeedDiagnosticTestOutOfNetworkProvider.location.topRight.x` | number |  |
| `fields.servicesYouMayNeedDiagnosticTestOutOfNetworkProvider.location.topRight.y` | number |  |
| `fields.servicesYouMayNeedDiagnosticTestOutOfNetworkProvider.type` | string |  |
| `fields.servicesYouMayNeedDiagnosticTestOutOfNetworkProvider.value` | string |  |
| `fields.servicesYouMayNeedDrugFormularyUrl.confidence` | number |  |
| `fields.servicesYouMayNeedDrugFormularyUrl.key` | string |  |
| `fields.servicesYouMayNeedDrugFormularyUrl.location.bottomLeft.x` | number |  |
| `fields.servicesYouMayNeedDrugFormularyUrl.location.bottomLeft.y` | number |  |
| `fields.servicesYouMayNeedDrugFormularyUrl.location.bottomRight.x` | number |  |
| `fields.servicesYouMayNeedDrugFormularyUrl.location.bottomRight.y` | number |  |
| `fields.servicesYouMayNeedDrugFormularyUrl.location.pageNumber` | number |  |
| `fields.servicesYouMayNeedDrugFormularyUrl.location.topLeft.x` | number |  |
| `fields.servicesYouMayNeedDrugFormularyUrl.location.topLeft.y` | number |  |
| `fields.servicesYouMayNeedDrugFormularyUrl.location.topRight.x` | number |  |
| `fields.servicesYouMayNeedDrugFormularyUrl.location.topRight.y` | number |  |
| `fields.servicesYouMayNeedDrugFormularyUrl.value` | string |  |
| `fields.servicesYouMayNeedDurableMedicalEquipmentInNetworkProvider.confidence` | number |  |
| `fields.servicesYouMayNeedDurableMedicalEquipmentInNetworkProvider.key` | string |  |
| `fields.servicesYouMayNeedDurableMedicalEquipmentInNetworkProvider.location.bottomLeft.x` | number |  |
| `fields.servicesYouMayNeedDurableMedicalEquipmentInNetworkProvider.location.bottomLeft.y` | number |  |
| `fields.servicesYouMayNeedDurableMedicalEquipmentInNetworkProvider.location.bottomRight.x` | number |  |
| `fields.servicesYouMayNeedDurableMedicalEquipmentInNetworkProvider.location.bottomRight.y` | number |  |
| `fields.servicesYouMayNeedDurableMedicalEquipmentInNetworkProvider.location.pageNumber` | number |  |
| `fields.servicesYouMayNeedDurableMedicalEquipmentInNetworkProvider.location.topLeft.x` | number |  |
| `fields.servicesYouMayNeedDurableMedicalEquipmentInNetworkProvider.location.topLeft.y` | number |  |
| `fields.servicesYouMayNeedDurableMedicalEquipmentInNetworkProvider.location.topRight.x` | number |  |
| `fields.servicesYouMayNeedDurableMedicalEquipmentInNetworkProvider.location.topRight.y` | number |  |
| `fields.servicesYouMayNeedDurableMedicalEquipmentInNetworkProvider.type` | string |  |
| `fields.servicesYouMayNeedDurableMedicalEquipmentInNetworkProvider.value` | string |  |
| `fields.servicesYouMayNeedDurableMedicalEquipmentOutOfNetworkProvider.confidence` | number |  |
| `fields.servicesYouMayNeedDurableMedicalEquipmentOutOfNetworkProvider.key` | string |  |
| `fields.servicesYouMayNeedDurableMedicalEquipmentOutOfNetworkProvider.location.bottomLeft.x` | number |  |
| `fields.servicesYouMayNeedDurableMedicalEquipmentOutOfNetworkProvider.location.bottomLeft.y` | number |  |
| `fields.servicesYouMayNeedDurableMedicalEquipmentOutOfNetworkProvider.location.bottomRight.x` | number |  |
| `fields.servicesYouMayNeedDurableMedicalEquipmentOutOfNetworkProvider.location.bottomRight.y` | number |  |
| `fields.servicesYouMayNeedDurableMedicalEquipmentOutOfNetworkProvider.location.pageNumber` | number |  |
| `fields.servicesYouMayNeedDurableMedicalEquipmentOutOfNetworkProvider.location.topLeft.x` | number |  |
| `fields.servicesYouMayNeedDurableMedicalEquipmentOutOfNetworkProvider.location.topLeft.y` | number |  |
| `fields.servicesYouMayNeedDurableMedicalEquipmentOutOfNetworkProvider.location.topRight.x` | number |  |
| `fields.servicesYouMayNeedDurableMedicalEquipmentOutOfNetworkProvider.location.topRight.y` | number |  |
| `fields.servicesYouMayNeedDurableMedicalEquipmentOutOfNetworkProvider.type` | string |  |
| `fields.servicesYouMayNeedDurableMedicalEquipmentOutOfNetworkProvider.value` | string |  |
| `fields.servicesYouMayNeedEmergencyMedicalTransportationInNetworkProvider.confidence` | number |  |
| `fields.servicesYouMayNeedEmergencyMedicalTransportationInNetworkProvider.key` | string |  |
| `fields.servicesYouMayNeedEmergencyMedicalTransportationInNetworkProvider.location.bottomLeft.x` | number |  |
| `fields.servicesYouMayNeedEmergencyMedicalTransportationInNetworkProvider.location.bottomLeft.y` | number |  |
| `fields.servicesYouMayNeedEmergencyMedicalTransportationInNetworkProvider.location.bottomRight.x` | number |  |
| `fields.servicesYouMayNeedEmergencyMedicalTransportationInNetworkProvider.location.bottomRight.y` | number |  |
| `fields.servicesYouMayNeedEmergencyMedicalTransportationInNetworkProvider.location.pageNumber` | number |  |
| `fields.servicesYouMayNeedEmergencyMedicalTransportationInNetworkProvider.location.topLeft.x` | number |  |
| `fields.servicesYouMayNeedEmergencyMedicalTransportationInNetworkProvider.location.topLeft.y` | number |  |
| `fields.servicesYouMayNeedEmergencyMedicalTransportationInNetworkProvider.location.topRight.x` | number |  |
| `fields.servicesYouMayNeedEmergencyMedicalTransportationInNetworkProvider.location.topRight.y` | number |  |
| `fields.servicesYouMayNeedEmergencyMedicalTransportationInNetworkProvider.type` | string |  |
| `fields.servicesYouMayNeedEmergencyMedicalTransportationInNetworkProvider.value` | string |  |
| `fields.servicesYouMayNeedEmergencyMedicalTransportationOutOfNetworkProvider.confidence` | number |  |
| `fields.servicesYouMayNeedEmergencyMedicalTransportationOutOfNetworkProvider.key` | string |  |
| `fields.servicesYouMayNeedEmergencyMedicalTransportationOutOfNetworkProvider.location.bottomLeft.x` | number |  |
| `fields.servicesYouMayNeedEmergencyMedicalTransportationOutOfNetworkProvider.location.bottomLeft.y` | number |  |
| `fields.servicesYouMayNeedEmergencyMedicalTransportationOutOfNetworkProvider.location.bottomRight.x` | number |  |
| `fields.servicesYouMayNeedEmergencyMedicalTransportationOutOfNetworkProvider.location.bottomRight.y` | number |  |
| `fields.servicesYouMayNeedEmergencyMedicalTransportationOutOfNetworkProvider.location.pageNumber` | number |  |
| `fields.servicesYouMayNeedEmergencyMedicalTransportationOutOfNetworkProvider.location.topLeft.x` | number |  |
| `fields.servicesYouMayNeedEmergencyMedicalTransportationOutOfNetworkProvider.location.topLeft.y` | number |  |
| `fields.servicesYouMayNeedEmergencyMedicalTransportationOutOfNetworkProvider.location.topRight.x` | number |  |
| `fields.servicesYouMayNeedEmergencyMedicalTransportationOutOfNetworkProvider.location.topRight.y` | number |  |
| `fields.servicesYouMayNeedEmergencyMedicalTransportationOutOfNetworkProvider.type` | string |  |
| `fields.servicesYouMayNeedEmergencyMedicalTransportationOutOfNetworkProvider.value` | string |  |
| `fields.servicesYouMayNeedEmergencyRoomCareInNetworkProvider.confidence` | number |  |
| `fields.servicesYouMayNeedEmergencyRoomCareInNetworkProvider.key` | string |  |
| `fields.servicesYouMayNeedEmergencyRoomCareInNetworkProvider.location.bottomLeft.x` | number |  |
| `fields.servicesYouMayNeedEmergencyRoomCareInNetworkProvider.location.bottomLeft.y` | number |  |
| `fields.servicesYouMayNeedEmergencyRoomCareInNetworkProvider.location.bottomRight.x` | number |  |
| `fields.servicesYouMayNeedEmergencyRoomCareInNetworkProvider.location.bottomRight.y` | number |  |
| `fields.servicesYouMayNeedEmergencyRoomCareInNetworkProvider.location.pageNumber` | number |  |
| `fields.servicesYouMayNeedEmergencyRoomCareInNetworkProvider.location.topLeft.x` | number |  |
| `fields.servicesYouMayNeedEmergencyRoomCareInNetworkProvider.location.topLeft.y` | number |  |
| `fields.servicesYouMayNeedEmergencyRoomCareInNetworkProvider.location.topRight.x` | number |  |
| `fields.servicesYouMayNeedEmergencyRoomCareInNetworkProvider.location.topRight.y` | number |  |
| `fields.servicesYouMayNeedEmergencyRoomCareInNetworkProvider.type` | string |  |
| `fields.servicesYouMayNeedEmergencyRoomCareInNetworkProvider.value` | string |  |
| `fields.servicesYouMayNeedEmergencyRoomCareOutOfNetworkProvider.confidence` | number |  |
| `fields.servicesYouMayNeedEmergencyRoomCareOutOfNetworkProvider.key` | string |  |
| `fields.servicesYouMayNeedEmergencyRoomCareOutOfNetworkProvider.location.bottomLeft.x` | number |  |
| `fields.servicesYouMayNeedEmergencyRoomCareOutOfNetworkProvider.location.bottomLeft.y` | number |  |
| `fields.servicesYouMayNeedEmergencyRoomCareOutOfNetworkProvider.location.bottomRight.x` | number |  |
| `fields.servicesYouMayNeedEmergencyRoomCareOutOfNetworkProvider.location.bottomRight.y` | number |  |
| `fields.servicesYouMayNeedEmergencyRoomCareOutOfNetworkProvider.location.pageNumber` | number |  |
| `fields.servicesYouMayNeedEmergencyRoomCareOutOfNetworkProvider.location.topLeft.x` | number |  |
| `fields.servicesYouMayNeedEmergencyRoomCareOutOfNetworkProvider.location.topLeft.y` | number |  |
| `fields.servicesYouMayNeedEmergencyRoomCareOutOfNetworkProvider.location.topRight.x` | number |  |
| `fields.servicesYouMayNeedEmergencyRoomCareOutOfNetworkProvider.location.topRight.y` | number |  |
| `fields.servicesYouMayNeedEmergencyRoomCareOutOfNetworkProvider.type` | string |  |
| `fields.servicesYouMayNeedEmergencyRoomCareOutOfNetworkProvider.value` | string |  |
| `fields.servicesYouMayNeedGenericDrugsInNetworkProvider.confidence` | number |  |
| `fields.servicesYouMayNeedGenericDrugsInNetworkProvider.key` | string |  |
| `fields.servicesYouMayNeedGenericDrugsInNetworkProvider.location.bottomLeft.x` | number |  |
| `fields.servicesYouMayNeedGenericDrugsInNetworkProvider.location.bottomLeft.y` | number |  |
| `fields.servicesYouMayNeedGenericDrugsInNetworkProvider.location.bottomRight.x` | number |  |
| `fields.servicesYouMayNeedGenericDrugsInNetworkProvider.location.bottomRight.y` | number |  |
| `fields.servicesYouMayNeedGenericDrugsInNetworkProvider.location.pageNumber` | number |  |
| `fields.servicesYouMayNeedGenericDrugsInNetworkProvider.location.topLeft.x` | number |  |
| `fields.servicesYouMayNeedGenericDrugsInNetworkProvider.location.topLeft.y` | number |  |
| `fields.servicesYouMayNeedGenericDrugsInNetworkProvider.location.topRight.x` | number |  |
| `fields.servicesYouMayNeedGenericDrugsInNetworkProvider.location.topRight.y` | number |  |
| `fields.servicesYouMayNeedGenericDrugsInNetworkProvider.type` | string |  |
| `fields.servicesYouMayNeedGenericDrugsInNetworkProvider.value` | string |  |
| `fields.servicesYouMayNeedGenericDrugsOutOfNetworkProvider.confidence` | number |  |
| `fields.servicesYouMayNeedGenericDrugsOutOfNetworkProvider.key` | string |  |
| `fields.servicesYouMayNeedGenericDrugsOutOfNetworkProvider.location.bottomLeft.x` | number |  |
| `fields.servicesYouMayNeedGenericDrugsOutOfNetworkProvider.location.bottomLeft.y` | number |  |
| `fields.servicesYouMayNeedGenericDrugsOutOfNetworkProvider.location.bottomRight.x` | number |  |
| `fields.servicesYouMayNeedGenericDrugsOutOfNetworkProvider.location.bottomRight.y` | number |  |
| `fields.servicesYouMayNeedGenericDrugsOutOfNetworkProvider.location.pageNumber` | number |  |
| `fields.servicesYouMayNeedGenericDrugsOutOfNetworkProvider.location.topLeft.x` | number |  |
| `fields.servicesYouMayNeedGenericDrugsOutOfNetworkProvider.location.topLeft.y` | number |  |
| `fields.servicesYouMayNeedGenericDrugsOutOfNetworkProvider.location.topRight.x` | number |  |
| `fields.servicesYouMayNeedGenericDrugsOutOfNetworkProvider.location.topRight.y` | number |  |
| `fields.servicesYouMayNeedGenericDrugsOutOfNetworkProvider.type` | string |  |
| `fields.servicesYouMayNeedGenericDrugsOutOfNetworkProvider.value` | string |  |
| `fields.servicesYouMayNeedHabilitationServicesInNetworkProvider.confidence` | number |  |
| `fields.servicesYouMayNeedHabilitationServicesInNetworkProvider.key` | string |  |
| `fields.servicesYouMayNeedHabilitationServicesInNetworkProvider.location.bottomLeft.x` | number |  |
| `fields.servicesYouMayNeedHabilitationServicesInNetworkProvider.location.bottomLeft.y` | number |  |
| `fields.servicesYouMayNeedHabilitationServicesInNetworkProvider.location.bottomRight.x` | number |  |
| `fields.servicesYouMayNeedHabilitationServicesInNetworkProvider.location.bottomRight.y` | number |  |
| `fields.servicesYouMayNeedHabilitationServicesInNetworkProvider.location.pageNumber` | number |  |
| `fields.servicesYouMayNeedHabilitationServicesInNetworkProvider.location.topLeft.x` | number |  |
| `fields.servicesYouMayNeedHabilitationServicesInNetworkProvider.location.topLeft.y` | number |  |
| `fields.servicesYouMayNeedHabilitationServicesInNetworkProvider.location.topRight.x` | number |  |
| `fields.servicesYouMayNeedHabilitationServicesInNetworkProvider.location.topRight.y` | number |  |
| `fields.servicesYouMayNeedHabilitationServicesInNetworkProvider.type` | string |  |
| `fields.servicesYouMayNeedHabilitationServicesInNetworkProvider.value` | string |  |
| `fields.servicesYouMayNeedHabilitationServicesOutOfNetworkProvider.confidence` | number |  |
| `fields.servicesYouMayNeedHabilitationServicesOutOfNetworkProvider.key` | string |  |
| `fields.servicesYouMayNeedHabilitationServicesOutOfNetworkProvider.location.bottomLeft.x` | number |  |
| `fields.servicesYouMayNeedHabilitationServicesOutOfNetworkProvider.location.bottomLeft.y` | number |  |
| `fields.servicesYouMayNeedHabilitationServicesOutOfNetworkProvider.location.bottomRight.x` | number |  |
| `fields.servicesYouMayNeedHabilitationServicesOutOfNetworkProvider.location.bottomRight.y` | number |  |
| `fields.servicesYouMayNeedHabilitationServicesOutOfNetworkProvider.location.pageNumber` | number |  |
| `fields.servicesYouMayNeedHabilitationServicesOutOfNetworkProvider.location.topLeft.x` | number |  |
| `fields.servicesYouMayNeedHabilitationServicesOutOfNetworkProvider.location.topLeft.y` | number |  |
| `fields.servicesYouMayNeedHabilitationServicesOutOfNetworkProvider.location.topRight.x` | number |  |
| `fields.servicesYouMayNeedHabilitationServicesOutOfNetworkProvider.location.topRight.y` | number |  |
| `fields.servicesYouMayNeedHabilitationServicesOutOfNetworkProvider.type` | string |  |
| `fields.servicesYouMayNeedHabilitationServicesOutOfNetworkProvider.value` | string |  |
| `fields.servicesYouMayNeedHomeHealthcareInNetworkProvider.confidence` | number |  |
| `fields.servicesYouMayNeedHomeHealthcareInNetworkProvider.key` | string |  |
| `fields.servicesYouMayNeedHomeHealthcareInNetworkProvider.location.bottomLeft.x` | number |  |
| `fields.servicesYouMayNeedHomeHealthcareInNetworkProvider.location.bottomLeft.y` | number |  |
| `fields.servicesYouMayNeedHomeHealthcareInNetworkProvider.location.bottomRight.x` | number |  |
| `fields.servicesYouMayNeedHomeHealthcareInNetworkProvider.location.bottomRight.y` | number |  |
| `fields.servicesYouMayNeedHomeHealthcareInNetworkProvider.location.pageNumber` | number |  |
| `fields.servicesYouMayNeedHomeHealthcareInNetworkProvider.location.topLeft.x` | number |  |
| `fields.servicesYouMayNeedHomeHealthcareInNetworkProvider.location.topLeft.y` | number |  |
| `fields.servicesYouMayNeedHomeHealthcareInNetworkProvider.location.topRight.x` | number |  |
| `fields.servicesYouMayNeedHomeHealthcareInNetworkProvider.location.topRight.y` | number |  |
| `fields.servicesYouMayNeedHomeHealthcareInNetworkProvider.type` | string |  |
| `fields.servicesYouMayNeedHomeHealthcareInNetworkProvider.value` | string |  |
| `fields.servicesYouMayNeedHomeHealthcareOutOfNetworkProvider.confidence` | number |  |
| `fields.servicesYouMayNeedHomeHealthcareOutOfNetworkProvider.key` | string |  |
| `fields.servicesYouMayNeedHomeHealthcareOutOfNetworkProvider.location.bottomLeft.x` | number |  |
| `fields.servicesYouMayNeedHomeHealthcareOutOfNetworkProvider.location.bottomLeft.y` | number |  |
| `fields.servicesYouMayNeedHomeHealthcareOutOfNetworkProvider.location.bottomRight.x` | number |  |
| `fields.servicesYouMayNeedHomeHealthcareOutOfNetworkProvider.location.bottomRight.y` | number |  |
| `fields.servicesYouMayNeedHomeHealthcareOutOfNetworkProvider.location.pageNumber` | number |  |
| `fields.servicesYouMayNeedHomeHealthcareOutOfNetworkProvider.location.topLeft.x` | number |  |
| `fields.servicesYouMayNeedHomeHealthcareOutOfNetworkProvider.location.topLeft.y` | number |  |
| `fields.servicesYouMayNeedHomeHealthcareOutOfNetworkProvider.location.topRight.x` | number |  |
| `fields.servicesYouMayNeedHomeHealthcareOutOfNetworkProvider.location.topRight.y` | number |  |
| `fields.servicesYouMayNeedHomeHealthcareOutOfNetworkProvider.type` | string |  |
| `fields.servicesYouMayNeedHomeHealthcareOutOfNetworkProvider.value` | string |  |
| `fields.servicesYouMayNeedHospiceServicesInNetworkProvider.confidence` | number |  |
| `fields.servicesYouMayNeedHospiceServicesInNetworkProvider.key` | string |  |
| `fields.servicesYouMayNeedHospiceServicesInNetworkProvider.location.bottomLeft.x` | number |  |
| `fields.servicesYouMayNeedHospiceServicesInNetworkProvider.location.bottomLeft.y` | number |  |
| `fields.servicesYouMayNeedHospiceServicesInNetworkProvider.location.bottomRight.x` | number |  |
| `fields.servicesYouMayNeedHospiceServicesInNetworkProvider.location.bottomRight.y` | number |  |
| `fields.servicesYouMayNeedHospiceServicesInNetworkProvider.location.pageNumber` | number |  |
| `fields.servicesYouMayNeedHospiceServicesInNetworkProvider.location.topLeft.x` | number |  |
| `fields.servicesYouMayNeedHospiceServicesInNetworkProvider.location.topLeft.y` | number |  |
| `fields.servicesYouMayNeedHospiceServicesInNetworkProvider.location.topRight.x` | number |  |
| `fields.servicesYouMayNeedHospiceServicesInNetworkProvider.location.topRight.y` | number |  |
| `fields.servicesYouMayNeedHospiceServicesInNetworkProvider.type` | string |  |
| `fields.servicesYouMayNeedHospiceServicesInNetworkProvider.value` | string |  |
| `fields.servicesYouMayNeedHospiceServicesOutOfNetworkProvider.confidence` | number |  |
| `fields.servicesYouMayNeedHospiceServicesOutOfNetworkProvider.key` | string |  |
| `fields.servicesYouMayNeedHospiceServicesOutOfNetworkProvider.location.bottomLeft.x` | number |  |
| `fields.servicesYouMayNeedHospiceServicesOutOfNetworkProvider.location.bottomLeft.y` | number |  |
| `fields.servicesYouMayNeedHospiceServicesOutOfNetworkProvider.location.bottomRight.x` | number |  |
| `fields.servicesYouMayNeedHospiceServicesOutOfNetworkProvider.location.bottomRight.y` | number |  |
| `fields.servicesYouMayNeedHospiceServicesOutOfNetworkProvider.location.pageNumber` | number |  |
| `fields.servicesYouMayNeedHospiceServicesOutOfNetworkProvider.location.topLeft.x` | number |  |
| `fields.servicesYouMayNeedHospiceServicesOutOfNetworkProvider.location.topLeft.y` | number |  |
| `fields.servicesYouMayNeedHospiceServicesOutOfNetworkProvider.location.topRight.x` | number |  |
| `fields.servicesYouMayNeedHospiceServicesOutOfNetworkProvider.location.topRight.y` | number |  |
| `fields.servicesYouMayNeedHospiceServicesOutOfNetworkProvider.type` | string |  |
| `fields.servicesYouMayNeedHospiceServicesOutOfNetworkProvider.value` | string |  |
| `fields.servicesYouMayNeedHospitalStayFacilityFeeInNetworkProvider.confidence` | number |  |
| `fields.servicesYouMayNeedHospitalStayFacilityFeeInNetworkProvider.key` | string |  |
| `fields.servicesYouMayNeedHospitalStayFacilityFeeInNetworkProvider.location.bottomLeft.x` | number |  |
| `fields.servicesYouMayNeedHospitalStayFacilityFeeInNetworkProvider.location.bottomLeft.y` | number |  |
| `fields.servicesYouMayNeedHospitalStayFacilityFeeInNetworkProvider.location.bottomRight.x` | number |  |
| `fields.servicesYouMayNeedHospitalStayFacilityFeeInNetworkProvider.location.bottomRight.y` | number |  |
| `fields.servicesYouMayNeedHospitalStayFacilityFeeInNetworkProvider.location.pageNumber` | number |  |
| `fields.servicesYouMayNeedHospitalStayFacilityFeeInNetworkProvider.location.topLeft.x` | number |  |
| `fields.servicesYouMayNeedHospitalStayFacilityFeeInNetworkProvider.location.topLeft.y` | number |  |
| `fields.servicesYouMayNeedHospitalStayFacilityFeeInNetworkProvider.location.topRight.x` | number |  |
| `fields.servicesYouMayNeedHospitalStayFacilityFeeInNetworkProvider.location.topRight.y` | number |  |
| `fields.servicesYouMayNeedHospitalStayFacilityFeeInNetworkProvider.type` | string |  |
| `fields.servicesYouMayNeedHospitalStayFacilityFeeInNetworkProvider.value` | string |  |
| `fields.servicesYouMayNeedHospitalStayFacilityFeeOutOfNetworkProvider.confidence` | number |  |
| `fields.servicesYouMayNeedHospitalStayFacilityFeeOutOfNetworkProvider.key` | string |  |
| `fields.servicesYouMayNeedHospitalStayFacilityFeeOutOfNetworkProvider.location.bottomLeft.x` | number |  |
| `fields.servicesYouMayNeedHospitalStayFacilityFeeOutOfNetworkProvider.location.bottomLeft.y` | number |  |
| `fields.servicesYouMayNeedHospitalStayFacilityFeeOutOfNetworkProvider.location.bottomRight.x` | number |  |
| `fields.servicesYouMayNeedHospitalStayFacilityFeeOutOfNetworkProvider.location.bottomRight.y` | number |  |
| `fields.servicesYouMayNeedHospitalStayFacilityFeeOutOfNetworkProvider.location.pageNumber` | number |  |
| `fields.servicesYouMayNeedHospitalStayFacilityFeeOutOfNetworkProvider.location.topLeft.x` | number |  |
| `fields.servicesYouMayNeedHospitalStayFacilityFeeOutOfNetworkProvider.location.topLeft.y` | number |  |
| `fields.servicesYouMayNeedHospitalStayFacilityFeeOutOfNetworkProvider.location.topRight.x` | number |  |
| `fields.servicesYouMayNeedHospitalStayFacilityFeeOutOfNetworkProvider.location.topRight.y` | number |  |
| `fields.servicesYouMayNeedHospitalStayFacilityFeeOutOfNetworkProvider.type` | string |  |
| `fields.servicesYouMayNeedHospitalStayFacilityFeeOutOfNetworkProvider.value` | string |  |
| `fields.servicesYouMayNeedHospitalStayPhysicianFeeInNetworkProvider.confidence` | number |  |
| `fields.servicesYouMayNeedHospitalStayPhysicianFeeInNetworkProvider.key` | string |  |
| `fields.servicesYouMayNeedHospitalStayPhysicianFeeInNetworkProvider.location.bottomLeft.x` | number |  |
| `fields.servicesYouMayNeedHospitalStayPhysicianFeeInNetworkProvider.location.bottomLeft.y` | number |  |
| `fields.servicesYouMayNeedHospitalStayPhysicianFeeInNetworkProvider.location.bottomRight.x` | number |  |
| `fields.servicesYouMayNeedHospitalStayPhysicianFeeInNetworkProvider.location.bottomRight.y` | number |  |
| `fields.servicesYouMayNeedHospitalStayPhysicianFeeInNetworkProvider.location.pageNumber` | number |  |
| `fields.servicesYouMayNeedHospitalStayPhysicianFeeInNetworkProvider.location.topLeft.x` | number |  |
| `fields.servicesYouMayNeedHospitalStayPhysicianFeeInNetworkProvider.location.topLeft.y` | number |  |
| `fields.servicesYouMayNeedHospitalStayPhysicianFeeInNetworkProvider.location.topRight.x` | number |  |
| `fields.servicesYouMayNeedHospitalStayPhysicianFeeInNetworkProvider.location.topRight.y` | number |  |
| `fields.servicesYouMayNeedHospitalStayPhysicianFeeInNetworkProvider.type` | string |  |
| `fields.servicesYouMayNeedHospitalStayPhysicianFeeInNetworkProvider.value` | string |  |
| `fields.servicesYouMayNeedHospitalStayPhysicianFeeOutOfNetworkProvider.confidence` | number |  |
| `fields.servicesYouMayNeedHospitalStayPhysicianFeeOutOfNetworkProvider.key` | string |  |
| `fields.servicesYouMayNeedHospitalStayPhysicianFeeOutOfNetworkProvider.location.bottomLeft.x` | number |  |
| `fields.servicesYouMayNeedHospitalStayPhysicianFeeOutOfNetworkProvider.location.bottomLeft.y` | number |  |
| `fields.servicesYouMayNeedHospitalStayPhysicianFeeOutOfNetworkProvider.location.bottomRight.x` | number |  |
| `fields.servicesYouMayNeedHospitalStayPhysicianFeeOutOfNetworkProvider.location.bottomRight.y` | number |  |
| `fields.servicesYouMayNeedHospitalStayPhysicianFeeOutOfNetworkProvider.location.pageNumber` | number |  |
| `fields.servicesYouMayNeedHospitalStayPhysicianFeeOutOfNetworkProvider.location.topLeft.x` | number |  |
| `fields.servicesYouMayNeedHospitalStayPhysicianFeeOutOfNetworkProvider.location.topLeft.y` | number |  |
| `fields.servicesYouMayNeedHospitalStayPhysicianFeeOutOfNetworkProvider.location.topRight.x` | number |  |
| `fields.servicesYouMayNeedHospitalStayPhysicianFeeOutOfNetworkProvider.location.topRight.y` | number |  |
| `fields.servicesYouMayNeedHospitalStayPhysicianFeeOutOfNetworkProvider.type` | string |  |
| `fields.servicesYouMayNeedHospitalStayPhysicianFeeOutOfNetworkProvider.value` | string |  |
| `fields.servicesYouMayNeedImagingInNetworkProvider.confidence` | number |  |
| `fields.servicesYouMayNeedImagingInNetworkProvider.key` | string |  |
| `fields.servicesYouMayNeedImagingInNetworkProvider.location.bottomLeft.x` | number |  |
| `fields.servicesYouMayNeedImagingInNetworkProvider.location.bottomLeft.y` | number |  |
| `fields.servicesYouMayNeedImagingInNetworkProvider.location.bottomRight.x` | number |  |
| `fields.servicesYouMayNeedImagingInNetworkProvider.location.bottomRight.y` | number |  |
| `fields.servicesYouMayNeedImagingInNetworkProvider.location.pageNumber` | number |  |
| `fields.servicesYouMayNeedImagingInNetworkProvider.location.topLeft.x` | number |  |
| `fields.servicesYouMayNeedImagingInNetworkProvider.location.topLeft.y` | number |  |
| `fields.servicesYouMayNeedImagingInNetworkProvider.location.topRight.x` | number |  |
| `fields.servicesYouMayNeedImagingInNetworkProvider.location.topRight.y` | number |  |
| `fields.servicesYouMayNeedImagingInNetworkProvider.type` | string |  |
| `fields.servicesYouMayNeedImagingInNetworkProvider.value` | string |  |
| `fields.servicesYouMayNeedImagingOutOfNetworkProvider.confidence` | number |  |
| `fields.servicesYouMayNeedImagingOutOfNetworkProvider.key` | string |  |
| `fields.servicesYouMayNeedImagingOutOfNetworkProvider.location.bottomLeft.x` | number |  |
| `fields.servicesYouMayNeedImagingOutOfNetworkProvider.location.bottomLeft.y` | number |  |
| `fields.servicesYouMayNeedImagingOutOfNetworkProvider.location.bottomRight.x` | number |  |
| `fields.servicesYouMayNeedImagingOutOfNetworkProvider.location.bottomRight.y` | number |  |
| `fields.servicesYouMayNeedImagingOutOfNetworkProvider.location.pageNumber` | number |  |
| `fields.servicesYouMayNeedImagingOutOfNetworkProvider.location.topLeft.x` | number |  |
| `fields.servicesYouMayNeedImagingOutOfNetworkProvider.location.topLeft.y` | number |  |
| `fields.servicesYouMayNeedImagingOutOfNetworkProvider.location.topRight.x` | number |  |
| `fields.servicesYouMayNeedImagingOutOfNetworkProvider.location.topRight.y` | number |  |
| `fields.servicesYouMayNeedImagingOutOfNetworkProvider.type` | string |  |
| `fields.servicesYouMayNeedImagingOutOfNetworkProvider.value` | string |  |
| `fields.servicesYouMayNeedInpatientMentalServicesInNetworkProvider.confidence` | number |  |
| `fields.servicesYouMayNeedInpatientMentalServicesInNetworkProvider.key` | string |  |
| `fields.servicesYouMayNeedInpatientMentalServicesInNetworkProvider.location.bottomLeft.x` | number |  |
| `fields.servicesYouMayNeedInpatientMentalServicesInNetworkProvider.location.bottomLeft.y` | number |  |
| `fields.servicesYouMayNeedInpatientMentalServicesInNetworkProvider.location.bottomRight.x` | number |  |
| `fields.servicesYouMayNeedInpatientMentalServicesInNetworkProvider.location.bottomRight.y` | number |  |
| `fields.servicesYouMayNeedInpatientMentalServicesInNetworkProvider.location.pageNumber` | number |  |
| `fields.servicesYouMayNeedInpatientMentalServicesInNetworkProvider.location.topLeft.x` | number |  |
| `fields.servicesYouMayNeedInpatientMentalServicesInNetworkProvider.location.topLeft.y` | number |  |
| `fields.servicesYouMayNeedInpatientMentalServicesInNetworkProvider.location.topRight.x` | number |  |
| `fields.servicesYouMayNeedInpatientMentalServicesInNetworkProvider.location.topRight.y` | number |  |
| `fields.servicesYouMayNeedInpatientMentalServicesInNetworkProvider.type` | string |  |
| `fields.servicesYouMayNeedInpatientMentalServicesInNetworkProvider.value` | string |  |
| `fields.servicesYouMayNeedInpatientMentalServicesOutOfNetworkProvider.confidence` | number |  |
| `fields.servicesYouMayNeedInpatientMentalServicesOutOfNetworkProvider.key` | string |  |
| `fields.servicesYouMayNeedInpatientMentalServicesOutOfNetworkProvider.location.bottomLeft.x` | number |  |
| `fields.servicesYouMayNeedInpatientMentalServicesOutOfNetworkProvider.location.bottomLeft.y` | number |  |
| `fields.servicesYouMayNeedInpatientMentalServicesOutOfNetworkProvider.location.bottomRight.x` | number |  |
| `fields.servicesYouMayNeedInpatientMentalServicesOutOfNetworkProvider.location.bottomRight.y` | number |  |
| `fields.servicesYouMayNeedInpatientMentalServicesOutOfNetworkProvider.location.pageNumber` | number |  |
| `fields.servicesYouMayNeedInpatientMentalServicesOutOfNetworkProvider.location.topLeft.x` | number |  |
| `fields.servicesYouMayNeedInpatientMentalServicesOutOfNetworkProvider.location.topLeft.y` | number |  |
| `fields.servicesYouMayNeedInpatientMentalServicesOutOfNetworkProvider.location.topRight.x` | number |  |
| `fields.servicesYouMayNeedInpatientMentalServicesOutOfNetworkProvider.location.topRight.y` | number |  |
| `fields.servicesYouMayNeedInpatientMentalServicesOutOfNetworkProvider.type` | string |  |
| `fields.servicesYouMayNeedInpatientMentalServicesOutOfNetworkProvider.value` | string |  |
| `fields.servicesYouMayNeedMailOrderDrugCoefficient.confidence` | number |  |
| `fields.servicesYouMayNeedMailOrderDrugCoefficient.key` | string |  |
| `fields.servicesYouMayNeedMailOrderDrugCoefficient.type` | string |  |
| `fields.servicesYouMayNeedMailOrderDrugCoefficient.value` | number |  |
| `fields.servicesYouMayNeedNonPreferredBrandDrugsInNetworkProvider.confidence` | number |  |
| `fields.servicesYouMayNeedNonPreferredBrandDrugsInNetworkProvider.key` | string |  |
| `fields.servicesYouMayNeedNonPreferredBrandDrugsInNetworkProvider.location.bottomLeft.x` | number |  |
| `fields.servicesYouMayNeedNonPreferredBrandDrugsInNetworkProvider.location.bottomLeft.y` | number |  |
| `fields.servicesYouMayNeedNonPreferredBrandDrugsInNetworkProvider.location.bottomRight.x` | number |  |
| `fields.servicesYouMayNeedNonPreferredBrandDrugsInNetworkProvider.location.bottomRight.y` | number |  |
| `fields.servicesYouMayNeedNonPreferredBrandDrugsInNetworkProvider.location.pageNumber` | number |  |
| `fields.servicesYouMayNeedNonPreferredBrandDrugsInNetworkProvider.location.topLeft.x` | number |  |
| `fields.servicesYouMayNeedNonPreferredBrandDrugsInNetworkProvider.location.topLeft.y` | number |  |
| `fields.servicesYouMayNeedNonPreferredBrandDrugsInNetworkProvider.location.topRight.x` | number |  |
| `fields.servicesYouMayNeedNonPreferredBrandDrugsInNetworkProvider.location.topRight.y` | number |  |
| `fields.servicesYouMayNeedNonPreferredBrandDrugsInNetworkProvider.type` | string |  |
| `fields.servicesYouMayNeedNonPreferredBrandDrugsInNetworkProvider.value` | string |  |
| `fields.servicesYouMayNeedNonPreferredBrandDrugsOutOfNetworkProvider.confidence` | number |  |
| `fields.servicesYouMayNeedNonPreferredBrandDrugsOutOfNetworkProvider.key` | string |  |
| `fields.servicesYouMayNeedNonPreferredBrandDrugsOutOfNetworkProvider.location.bottomLeft.x` | number |  |
| `fields.servicesYouMayNeedNonPreferredBrandDrugsOutOfNetworkProvider.location.bottomLeft.y` | number |  |
| `fields.servicesYouMayNeedNonPreferredBrandDrugsOutOfNetworkProvider.location.bottomRight.x` | number |  |
| `fields.servicesYouMayNeedNonPreferredBrandDrugsOutOfNetworkProvider.location.bottomRight.y` | number |  |
| `fields.servicesYouMayNeedNonPreferredBrandDrugsOutOfNetworkProvider.location.pageNumber` | number |  |
| `fields.servicesYouMayNeedNonPreferredBrandDrugsOutOfNetworkProvider.location.topLeft.x` | number |  |
| `fields.servicesYouMayNeedNonPreferredBrandDrugsOutOfNetworkProvider.location.topLeft.y` | number |  |
| `fields.servicesYouMayNeedNonPreferredBrandDrugsOutOfNetworkProvider.location.topRight.x` | number |  |
| `fields.servicesYouMayNeedNonPreferredBrandDrugsOutOfNetworkProvider.location.topRight.y` | number |  |
| `fields.servicesYouMayNeedNonPreferredBrandDrugsOutOfNetworkProvider.type` | string |  |
| `fields.servicesYouMayNeedNonPreferredBrandDrugsOutOfNetworkProvider.value` | string |  |
| `fields.servicesYouMayNeedOutOfNetworkCoverage.confidence` | number |  |
| `fields.servicesYouMayNeedOutOfNetworkCoverage.key` | string |  |
| `fields.servicesYouMayNeedOutOfNetworkCoverage.type` | string |  |
| `fields.servicesYouMayNeedOutOfNetworkCoverage.value` | string |  |
| `fields.servicesYouMayNeedOutpatientFacilityFeeInNetworkProvider.confidence` | number |  |
| `fields.servicesYouMayNeedOutpatientFacilityFeeInNetworkProvider.key` | string |  |
| `fields.servicesYouMayNeedOutpatientFacilityFeeInNetworkProvider.location.bottomLeft.x` | number |  |
| `fields.servicesYouMayNeedOutpatientFacilityFeeInNetworkProvider.location.bottomLeft.y` | number |  |
| `fields.servicesYouMayNeedOutpatientFacilityFeeInNetworkProvider.location.bottomRight.x` | number |  |
| `fields.servicesYouMayNeedOutpatientFacilityFeeInNetworkProvider.location.bottomRight.y` | number |  |
| `fields.servicesYouMayNeedOutpatientFacilityFeeInNetworkProvider.location.pageNumber` | number |  |
| `fields.servicesYouMayNeedOutpatientFacilityFeeInNetworkProvider.location.topLeft.x` | number |  |
| `fields.servicesYouMayNeedOutpatientFacilityFeeInNetworkProvider.location.topLeft.y` | number |  |
| `fields.servicesYouMayNeedOutpatientFacilityFeeInNetworkProvider.location.topRight.x` | number |  |
| `fields.servicesYouMayNeedOutpatientFacilityFeeInNetworkProvider.location.topRight.y` | number |  |
| `fields.servicesYouMayNeedOutpatientFacilityFeeInNetworkProvider.type` | string |  |
| `fields.servicesYouMayNeedOutpatientFacilityFeeInNetworkProvider.value` | string |  |
| `fields.servicesYouMayNeedOutpatientFacilityFeeOutOfNetworkProvider.confidence` | number |  |
| `fields.servicesYouMayNeedOutpatientFacilityFeeOutOfNetworkProvider.key` | string |  |
| `fields.servicesYouMayNeedOutpatientFacilityFeeOutOfNetworkProvider.location.bottomLeft.x` | number |  |
| `fields.servicesYouMayNeedOutpatientFacilityFeeOutOfNetworkProvider.location.bottomLeft.y` | number |  |
| `fields.servicesYouMayNeedOutpatientFacilityFeeOutOfNetworkProvider.location.bottomRight.x` | number |  |
| `fields.servicesYouMayNeedOutpatientFacilityFeeOutOfNetworkProvider.location.bottomRight.y` | number |  |
| `fields.servicesYouMayNeedOutpatientFacilityFeeOutOfNetworkProvider.location.pageNumber` | number |  |
| `fields.servicesYouMayNeedOutpatientFacilityFeeOutOfNetworkProvider.location.topLeft.x` | number |  |
| `fields.servicesYouMayNeedOutpatientFacilityFeeOutOfNetworkProvider.location.topLeft.y` | number |  |
| `fields.servicesYouMayNeedOutpatientFacilityFeeOutOfNetworkProvider.location.topRight.x` | number |  |
| `fields.servicesYouMayNeedOutpatientFacilityFeeOutOfNetworkProvider.location.topRight.y` | number |  |
| `fields.servicesYouMayNeedOutpatientFacilityFeeOutOfNetworkProvider.type` | string |  |
| `fields.servicesYouMayNeedOutpatientFacilityFeeOutOfNetworkProvider.value` | string |  |
| `fields.servicesYouMayNeedOutpatientMentalServicesInNetworkProvider.confidence` | number |  |
| `fields.servicesYouMayNeedOutpatientMentalServicesInNetworkProvider.key` | string |  |
| `fields.servicesYouMayNeedOutpatientMentalServicesInNetworkProvider.location.bottomLeft.x` | number |  |
| `fields.servicesYouMayNeedOutpatientMentalServicesInNetworkProvider.location.bottomLeft.y` | number |  |
| `fields.servicesYouMayNeedOutpatientMentalServicesInNetworkProvider.location.bottomRight.x` | number |  |
| `fields.servicesYouMayNeedOutpatientMentalServicesInNetworkProvider.location.bottomRight.y` | number |  |
| `fields.servicesYouMayNeedOutpatientMentalServicesInNetworkProvider.location.pageNumber` | number |  |
| `fields.servicesYouMayNeedOutpatientMentalServicesInNetworkProvider.location.topLeft.x` | number |  |
| `fields.servicesYouMayNeedOutpatientMentalServicesInNetworkProvider.location.topLeft.y` | number |  |
| `fields.servicesYouMayNeedOutpatientMentalServicesInNetworkProvider.location.topRight.x` | number |  |
| `fields.servicesYouMayNeedOutpatientMentalServicesInNetworkProvider.location.topRight.y` | number |  |
| `fields.servicesYouMayNeedOutpatientMentalServicesInNetworkProvider.type` | string |  |
| `fields.servicesYouMayNeedOutpatientMentalServicesInNetworkProvider.value` | string |  |
| `fields.servicesYouMayNeedOutpatientMentalServicesOutOfNetworkProvider.confidence` | number |  |
| `fields.servicesYouMayNeedOutpatientMentalServicesOutOfNetworkProvider.key` | string |  |
| `fields.servicesYouMayNeedOutpatientMentalServicesOutOfNetworkProvider.location.bottomLeft.x` | number |  |
| `fields.servicesYouMayNeedOutpatientMentalServicesOutOfNetworkProvider.location.bottomLeft.y` | number |  |
| `fields.servicesYouMayNeedOutpatientMentalServicesOutOfNetworkProvider.location.bottomRight.x` | number |  |
| `fields.servicesYouMayNeedOutpatientMentalServicesOutOfNetworkProvider.location.bottomRight.y` | number |  |
| `fields.servicesYouMayNeedOutpatientMentalServicesOutOfNetworkProvider.location.pageNumber` | number |  |
| `fields.servicesYouMayNeedOutpatientMentalServicesOutOfNetworkProvider.location.topLeft.x` | number |  |
| `fields.servicesYouMayNeedOutpatientMentalServicesOutOfNetworkProvider.location.topLeft.y` | number |  |
| `fields.servicesYouMayNeedOutpatientMentalServicesOutOfNetworkProvider.location.topRight.x` | number |  |
| `fields.servicesYouMayNeedOutpatientMentalServicesOutOfNetworkProvider.location.topRight.y` | number |  |
| `fields.servicesYouMayNeedOutpatientMentalServicesOutOfNetworkProvider.type` | string |  |
| `fields.servicesYouMayNeedOutpatientMentalServicesOutOfNetworkProvider.value` | string |  |
| `fields.servicesYouMayNeedOutpatientPhysicianFeeInNetworkProvider.confidence` | number |  |
| `fields.servicesYouMayNeedOutpatientPhysicianFeeInNetworkProvider.key` | string |  |
| `fields.servicesYouMayNeedOutpatientPhysicianFeeInNetworkProvider.location.bottomLeft.x` | number |  |
| `fields.servicesYouMayNeedOutpatientPhysicianFeeInNetworkProvider.location.bottomLeft.y` | number |  |
| `fields.servicesYouMayNeedOutpatientPhysicianFeeInNetworkProvider.location.bottomRight.x` | number |  |
| `fields.servicesYouMayNeedOutpatientPhysicianFeeInNetworkProvider.location.bottomRight.y` | number |  |
| `fields.servicesYouMayNeedOutpatientPhysicianFeeInNetworkProvider.location.pageNumber` | number |  |
| `fields.servicesYouMayNeedOutpatientPhysicianFeeInNetworkProvider.location.topLeft.x` | number |  |
| `fields.servicesYouMayNeedOutpatientPhysicianFeeInNetworkProvider.location.topLeft.y` | number |  |
| `fields.servicesYouMayNeedOutpatientPhysicianFeeInNetworkProvider.location.topRight.x` | number |  |
| `fields.servicesYouMayNeedOutpatientPhysicianFeeInNetworkProvider.location.topRight.y` | number |  |
| `fields.servicesYouMayNeedOutpatientPhysicianFeeInNetworkProvider.type` | string |  |
| `fields.servicesYouMayNeedOutpatientPhysicianFeeInNetworkProvider.value` | string |  |
| `fields.servicesYouMayNeedOutpatientPhysicianFeeOutOfNetworkProvider.confidence` | number |  |
| `fields.servicesYouMayNeedOutpatientPhysicianFeeOutOfNetworkProvider.key` | string |  |
| `fields.servicesYouMayNeedOutpatientPhysicianFeeOutOfNetworkProvider.location.bottomLeft.x` | number |  |
| `fields.servicesYouMayNeedOutpatientPhysicianFeeOutOfNetworkProvider.location.bottomLeft.y` | number |  |
| `fields.servicesYouMayNeedOutpatientPhysicianFeeOutOfNetworkProvider.location.bottomRight.x` | number |  |
| `fields.servicesYouMayNeedOutpatientPhysicianFeeOutOfNetworkProvider.location.bottomRight.y` | number |  |
| `fields.servicesYouMayNeedOutpatientPhysicianFeeOutOfNetworkProvider.location.pageNumber` | number |  |
| `fields.servicesYouMayNeedOutpatientPhysicianFeeOutOfNetworkProvider.location.topLeft.x` | number |  |
| `fields.servicesYouMayNeedOutpatientPhysicianFeeOutOfNetworkProvider.location.topLeft.y` | number |  |
| `fields.servicesYouMayNeedOutpatientPhysicianFeeOutOfNetworkProvider.location.topRight.x` | number |  |
| `fields.servicesYouMayNeedOutpatientPhysicianFeeOutOfNetworkProvider.location.topRight.y` | number |  |
| `fields.servicesYouMayNeedOutpatientPhysicianFeeOutOfNetworkProvider.type` | string |  |
| `fields.servicesYouMayNeedOutpatientPhysicianFeeOutOfNetworkProvider.value` | string |  |
| `fields.servicesYouMayNeedPreferredBrandDrugsInNetworkProvider.confidence` | number |  |
| `fields.servicesYouMayNeedPreferredBrandDrugsInNetworkProvider.key` | string |  |
| `fields.servicesYouMayNeedPreferredBrandDrugsInNetworkProvider.location.bottomLeft.x` | number |  |
| `fields.servicesYouMayNeedPreferredBrandDrugsInNetworkProvider.location.bottomLeft.y` | number |  |
| `fields.servicesYouMayNeedPreferredBrandDrugsInNetworkProvider.location.bottomRight.x` | number |  |
| `fields.servicesYouMayNeedPreferredBrandDrugsInNetworkProvider.location.bottomRight.y` | number |  |
| `fields.servicesYouMayNeedPreferredBrandDrugsInNetworkProvider.location.pageNumber` | number |  |
| `fields.servicesYouMayNeedPreferredBrandDrugsInNetworkProvider.location.topLeft.x` | number |  |
| `fields.servicesYouMayNeedPreferredBrandDrugsInNetworkProvider.location.topLeft.y` | number |  |
| `fields.servicesYouMayNeedPreferredBrandDrugsInNetworkProvider.location.topRight.x` | number |  |
| `fields.servicesYouMayNeedPreferredBrandDrugsInNetworkProvider.location.topRight.y` | number |  |
| `fields.servicesYouMayNeedPreferredBrandDrugsInNetworkProvider.type` | string |  |
| `fields.servicesYouMayNeedPreferredBrandDrugsInNetworkProvider.value` | string |  |
| `fields.servicesYouMayNeedPreferredBrandDrugsOutOfNetworkProvider.confidence` | number |  |
| `fields.servicesYouMayNeedPreferredBrandDrugsOutOfNetworkProvider.key` | string |  |
| `fields.servicesYouMayNeedPreferredBrandDrugsOutOfNetworkProvider.location.bottomLeft.x` | number |  |
| `fields.servicesYouMayNeedPreferredBrandDrugsOutOfNetworkProvider.location.bottomLeft.y` | number |  |
| `fields.servicesYouMayNeedPreferredBrandDrugsOutOfNetworkProvider.location.bottomRight.x` | number |  |
| `fields.servicesYouMayNeedPreferredBrandDrugsOutOfNetworkProvider.location.bottomRight.y` | number |  |
| `fields.servicesYouMayNeedPreferredBrandDrugsOutOfNetworkProvider.location.pageNumber` | number |  |
| `fields.servicesYouMayNeedPreferredBrandDrugsOutOfNetworkProvider.location.topLeft.x` | number |  |
| `fields.servicesYouMayNeedPreferredBrandDrugsOutOfNetworkProvider.location.topLeft.y` | number |  |
| `fields.servicesYouMayNeedPreferredBrandDrugsOutOfNetworkProvider.location.topRight.x` | number |  |
| `fields.servicesYouMayNeedPreferredBrandDrugsOutOfNetworkProvider.location.topRight.y` | number |  |
| `fields.servicesYouMayNeedPreferredBrandDrugsOutOfNetworkProvider.type` | string |  |
| `fields.servicesYouMayNeedPreferredBrandDrugsOutOfNetworkProvider.value` | string |  |
| `fields.servicesYouMayNeedPreventiveCareInNetworkProvider.confidence` | number |  |
| `fields.servicesYouMayNeedPreventiveCareInNetworkProvider.key` | string |  |
| `fields.servicesYouMayNeedPreventiveCareInNetworkProvider.location.bottomLeft.x` | number |  |
| `fields.servicesYouMayNeedPreventiveCareInNetworkProvider.location.bottomLeft.y` | number |  |
| `fields.servicesYouMayNeedPreventiveCareInNetworkProvider.location.bottomRight.x` | number |  |
| `fields.servicesYouMayNeedPreventiveCareInNetworkProvider.location.bottomRight.y` | number |  |
| `fields.servicesYouMayNeedPreventiveCareInNetworkProvider.location.pageNumber` | number |  |
| `fields.servicesYouMayNeedPreventiveCareInNetworkProvider.location.topLeft.x` | number |  |
| `fields.servicesYouMayNeedPreventiveCareInNetworkProvider.location.topLeft.y` | number |  |
| `fields.servicesYouMayNeedPreventiveCareInNetworkProvider.location.topRight.x` | number |  |
| `fields.servicesYouMayNeedPreventiveCareInNetworkProvider.location.topRight.y` | number |  |
| `fields.servicesYouMayNeedPreventiveCareInNetworkProvider.type` | string |  |
| `fields.servicesYouMayNeedPreventiveCareInNetworkProvider.value` | string |  |
| `fields.servicesYouMayNeedPreventiveCareOutOfNetworkProvider.confidence` | number |  |
| `fields.servicesYouMayNeedPreventiveCareOutOfNetworkProvider.key` | string |  |
| `fields.servicesYouMayNeedPreventiveCareOutOfNetworkProvider.location.bottomLeft.x` | number |  |
| `fields.servicesYouMayNeedPreventiveCareOutOfNetworkProvider.location.bottomLeft.y` | number |  |
| `fields.servicesYouMayNeedPreventiveCareOutOfNetworkProvider.location.bottomRight.x` | number |  |
| `fields.servicesYouMayNeedPreventiveCareOutOfNetworkProvider.location.bottomRight.y` | number |  |
| `fields.servicesYouMayNeedPreventiveCareOutOfNetworkProvider.location.pageNumber` | number |  |
| `fields.servicesYouMayNeedPreventiveCareOutOfNetworkProvider.location.topLeft.x` | number |  |
| `fields.servicesYouMayNeedPreventiveCareOutOfNetworkProvider.location.topLeft.y` | number |  |
| `fields.servicesYouMayNeedPreventiveCareOutOfNetworkProvider.location.topRight.x` | number |  |
| `fields.servicesYouMayNeedPreventiveCareOutOfNetworkProvider.location.topRight.y` | number |  |
| `fields.servicesYouMayNeedPreventiveCareOutOfNetworkProvider.type` | string |  |
| `fields.servicesYouMayNeedPreventiveCareOutOfNetworkProvider.value` | string |  |
| `fields.servicesYouMayNeedPrimaryCareInNetworkProvider.confidence` | number |  |
| `fields.servicesYouMayNeedPrimaryCareInNetworkProvider.key` | string |  |
| `fields.servicesYouMayNeedPrimaryCareInNetworkProvider.location.bottomLeft.x` | number |  |
| `fields.servicesYouMayNeedPrimaryCareInNetworkProvider.location.bottomLeft.y` | number |  |
| `fields.servicesYouMayNeedPrimaryCareInNetworkProvider.location.bottomRight.x` | number |  |
| `fields.servicesYouMayNeedPrimaryCareInNetworkProvider.location.bottomRight.y` | number |  |
| `fields.servicesYouMayNeedPrimaryCareInNetworkProvider.location.pageNumber` | number |  |
| `fields.servicesYouMayNeedPrimaryCareInNetworkProvider.location.topLeft.x` | number |  |
| `fields.servicesYouMayNeedPrimaryCareInNetworkProvider.location.topLeft.y` | number |  |
| `fields.servicesYouMayNeedPrimaryCareInNetworkProvider.location.topRight.x` | number |  |
| `fields.servicesYouMayNeedPrimaryCareInNetworkProvider.location.topRight.y` | number |  |
| `fields.servicesYouMayNeedPrimaryCareInNetworkProvider.type` | string |  |
| `fields.servicesYouMayNeedPrimaryCareInNetworkProvider.value` | string |  |
| `fields.servicesYouMayNeedPrimaryCareOutOfNetworkProvider.confidence` | number |  |
| `fields.servicesYouMayNeedPrimaryCareOutOfNetworkProvider.key` | string |  |
| `fields.servicesYouMayNeedPrimaryCareOutOfNetworkProvider.location.bottomLeft.x` | number |  |
| `fields.servicesYouMayNeedPrimaryCareOutOfNetworkProvider.location.bottomLeft.y` | number |  |
| `fields.servicesYouMayNeedPrimaryCareOutOfNetworkProvider.location.bottomRight.x` | number |  |
| `fields.servicesYouMayNeedPrimaryCareOutOfNetworkProvider.location.bottomRight.y` | number |  |
| `fields.servicesYouMayNeedPrimaryCareOutOfNetworkProvider.location.pageNumber` | number |  |
| `fields.servicesYouMayNeedPrimaryCareOutOfNetworkProvider.location.topLeft.x` | number |  |
| `fields.servicesYouMayNeedPrimaryCareOutOfNetworkProvider.location.topLeft.y` | number |  |
| `fields.servicesYouMayNeedPrimaryCareOutOfNetworkProvider.location.topRight.x` | number |  |
| `fields.servicesYouMayNeedPrimaryCareOutOfNetworkProvider.location.topRight.y` | number |  |
| `fields.servicesYouMayNeedPrimaryCareOutOfNetworkProvider.type` | string |  |
| `fields.servicesYouMayNeedPrimaryCareOutOfNetworkProvider.value` | string |  |
| `fields.servicesYouMayNeedRehabilitationServicesInNetworkProvider.confidence` | number |  |
| `fields.servicesYouMayNeedRehabilitationServicesInNetworkProvider.key` | string |  |
| `fields.servicesYouMayNeedRehabilitationServicesInNetworkProvider.location.bottomLeft.x` | number |  |
| `fields.servicesYouMayNeedRehabilitationServicesInNetworkProvider.location.bottomLeft.y` | number |  |
| `fields.servicesYouMayNeedRehabilitationServicesInNetworkProvider.location.bottomRight.x` | number |  |
| `fields.servicesYouMayNeedRehabilitationServicesInNetworkProvider.location.bottomRight.y` | number |  |
| `fields.servicesYouMayNeedRehabilitationServicesInNetworkProvider.location.pageNumber` | number |  |
| `fields.servicesYouMayNeedRehabilitationServicesInNetworkProvider.location.topLeft.x` | number |  |
| `fields.servicesYouMayNeedRehabilitationServicesInNetworkProvider.location.topLeft.y` | number |  |
| `fields.servicesYouMayNeedRehabilitationServicesInNetworkProvider.location.topRight.x` | number |  |
| `fields.servicesYouMayNeedRehabilitationServicesInNetworkProvider.location.topRight.y` | number |  |
| `fields.servicesYouMayNeedRehabilitationServicesInNetworkProvider.type` | string |  |
| `fields.servicesYouMayNeedRehabilitationServicesInNetworkProvider.value` | string |  |
| `fields.servicesYouMayNeedRehabilitationServicesOutOfNetworkProvider.confidence` | number |  |
| `fields.servicesYouMayNeedRehabilitationServicesOutOfNetworkProvider.key` | string |  |
| `fields.servicesYouMayNeedRehabilitationServicesOutOfNetworkProvider.location.bottomLeft.x` | number |  |
| `fields.servicesYouMayNeedRehabilitationServicesOutOfNetworkProvider.location.bottomLeft.y` | number |  |
| `fields.servicesYouMayNeedRehabilitationServicesOutOfNetworkProvider.location.bottomRight.x` | number |  |
| `fields.servicesYouMayNeedRehabilitationServicesOutOfNetworkProvider.location.bottomRight.y` | number |  |
| `fields.servicesYouMayNeedRehabilitationServicesOutOfNetworkProvider.location.pageNumber` | number |  |
| `fields.servicesYouMayNeedRehabilitationServicesOutOfNetworkProvider.location.topLeft.x` | number |  |
| `fields.servicesYouMayNeedRehabilitationServicesOutOfNetworkProvider.location.topLeft.y` | number |  |
| `fields.servicesYouMayNeedRehabilitationServicesOutOfNetworkProvider.location.topRight.x` | number |  |
| `fields.servicesYouMayNeedRehabilitationServicesOutOfNetworkProvider.location.topRight.y` | number |  |
| `fields.servicesYouMayNeedRehabilitationServicesOutOfNetworkProvider.type` | string |  |
| `fields.servicesYouMayNeedRehabilitationServicesOutOfNetworkProvider.value` | string |  |
| `fields.servicesYouMayNeedSkilledNursingCareInNetworkProvider.confidence` | number |  |
| `fields.servicesYouMayNeedSkilledNursingCareInNetworkProvider.key` | string |  |
| `fields.servicesYouMayNeedSkilledNursingCareInNetworkProvider.location.bottomLeft.x` | number |  |
| `fields.servicesYouMayNeedSkilledNursingCareInNetworkProvider.location.bottomLeft.y` | number |  |
| `fields.servicesYouMayNeedSkilledNursingCareInNetworkProvider.location.bottomRight.x` | number |  |
| `fields.servicesYouMayNeedSkilledNursingCareInNetworkProvider.location.bottomRight.y` | number |  |
| `fields.servicesYouMayNeedSkilledNursingCareInNetworkProvider.location.pageNumber` | number |  |
| `fields.servicesYouMayNeedSkilledNursingCareInNetworkProvider.location.topLeft.x` | number |  |
| `fields.servicesYouMayNeedSkilledNursingCareInNetworkProvider.location.topLeft.y` | number |  |
| `fields.servicesYouMayNeedSkilledNursingCareInNetworkProvider.location.topRight.x` | number |  |
| `fields.servicesYouMayNeedSkilledNursingCareInNetworkProvider.location.topRight.y` | number |  |
| `fields.servicesYouMayNeedSkilledNursingCareInNetworkProvider.type` | string |  |
| `fields.servicesYouMayNeedSkilledNursingCareInNetworkProvider.value` | string |  |
| `fields.servicesYouMayNeedSkilledNursingCareOutOfNetworkProvider.confidence` | number |  |
| `fields.servicesYouMayNeedSkilledNursingCareOutOfNetworkProvider.key` | string |  |
| `fields.servicesYouMayNeedSkilledNursingCareOutOfNetworkProvider.location.bottomLeft.x` | number |  |
| `fields.servicesYouMayNeedSkilledNursingCareOutOfNetworkProvider.location.bottomLeft.y` | number |  |
| `fields.servicesYouMayNeedSkilledNursingCareOutOfNetworkProvider.location.bottomRight.x` | number |  |
| `fields.servicesYouMayNeedSkilledNursingCareOutOfNetworkProvider.location.bottomRight.y` | number |  |
| `fields.servicesYouMayNeedSkilledNursingCareOutOfNetworkProvider.location.pageNumber` | number |  |
| `fields.servicesYouMayNeedSkilledNursingCareOutOfNetworkProvider.location.topLeft.x` | number |  |
| `fields.servicesYouMayNeedSkilledNursingCareOutOfNetworkProvider.location.topLeft.y` | number |  |
| `fields.servicesYouMayNeedSkilledNursingCareOutOfNetworkProvider.location.topRight.x` | number |  |
| `fields.servicesYouMayNeedSkilledNursingCareOutOfNetworkProvider.location.topRight.y` | number |  |
| `fields.servicesYouMayNeedSkilledNursingCareOutOfNetworkProvider.type` | string |  |
| `fields.servicesYouMayNeedSkilledNursingCareOutOfNetworkProvider.value` | string |  |
| `fields.servicesYouMayNeedSpecialistVisitInNetworkProvider.confidence` | number |  |
| `fields.servicesYouMayNeedSpecialistVisitInNetworkProvider.key` | string |  |
| `fields.servicesYouMayNeedSpecialistVisitInNetworkProvider.location.bottomLeft.x` | number |  |
| `fields.servicesYouMayNeedSpecialistVisitInNetworkProvider.location.bottomLeft.y` | number |  |
| `fields.servicesYouMayNeedSpecialistVisitInNetworkProvider.location.bottomRight.x` | number |  |
| `fields.servicesYouMayNeedSpecialistVisitInNetworkProvider.location.bottomRight.y` | number |  |
| `fields.servicesYouMayNeedSpecialistVisitInNetworkProvider.location.pageNumber` | number |  |
| `fields.servicesYouMayNeedSpecialistVisitInNetworkProvider.location.topLeft.x` | number |  |
| `fields.servicesYouMayNeedSpecialistVisitInNetworkProvider.location.topLeft.y` | number |  |
| `fields.servicesYouMayNeedSpecialistVisitInNetworkProvider.location.topRight.x` | number |  |
| `fields.servicesYouMayNeedSpecialistVisitInNetworkProvider.location.topRight.y` | number |  |
| `fields.servicesYouMayNeedSpecialistVisitInNetworkProvider.type` | string |  |
| `fields.servicesYouMayNeedSpecialistVisitInNetworkProvider.value` | string |  |
| `fields.servicesYouMayNeedSpecialistVisitOutOfNetworkProvider.confidence` | number |  |
| `fields.servicesYouMayNeedSpecialistVisitOutOfNetworkProvider.key` | string |  |
| `fields.servicesYouMayNeedSpecialistVisitOutOfNetworkProvider.location.bottomLeft.x` | number |  |
| `fields.servicesYouMayNeedSpecialistVisitOutOfNetworkProvider.location.bottomLeft.y` | number |  |
| `fields.servicesYouMayNeedSpecialistVisitOutOfNetworkProvider.location.bottomRight.x` | number |  |
| `fields.servicesYouMayNeedSpecialistVisitOutOfNetworkProvider.location.bottomRight.y` | number |  |
| `fields.servicesYouMayNeedSpecialistVisitOutOfNetworkProvider.location.pageNumber` | number |  |
| `fields.servicesYouMayNeedSpecialistVisitOutOfNetworkProvider.location.topLeft.x` | number |  |
| `fields.servicesYouMayNeedSpecialistVisitOutOfNetworkProvider.location.topLeft.y` | number |  |
| `fields.servicesYouMayNeedSpecialistVisitOutOfNetworkProvider.location.topRight.x` | number |  |
| `fields.servicesYouMayNeedSpecialistVisitOutOfNetworkProvider.location.topRight.y` | number |  |
| `fields.servicesYouMayNeedSpecialistVisitOutOfNetworkProvider.type` | string |  |
| `fields.servicesYouMayNeedSpecialistVisitOutOfNetworkProvider.value` | string |  |
| `fields.servicesYouMayNeedSpecialtyDrugsInNetworkProvider.confidence` | number |  |
| `fields.servicesYouMayNeedSpecialtyDrugsInNetworkProvider.key` | string |  |
| `fields.servicesYouMayNeedSpecialtyDrugsInNetworkProvider.location.bottomLeft.x` | number |  |
| `fields.servicesYouMayNeedSpecialtyDrugsInNetworkProvider.location.bottomLeft.y` | number |  |
| `fields.servicesYouMayNeedSpecialtyDrugsInNetworkProvider.location.bottomRight.x` | number |  |
| `fields.servicesYouMayNeedSpecialtyDrugsInNetworkProvider.location.bottomRight.y` | number |  |
| `fields.servicesYouMayNeedSpecialtyDrugsInNetworkProvider.location.pageNumber` | number |  |
| `fields.servicesYouMayNeedSpecialtyDrugsInNetworkProvider.location.topLeft.x` | number |  |
| `fields.servicesYouMayNeedSpecialtyDrugsInNetworkProvider.location.topLeft.y` | number |  |
| `fields.servicesYouMayNeedSpecialtyDrugsInNetworkProvider.location.topRight.x` | number |  |
| `fields.servicesYouMayNeedSpecialtyDrugsInNetworkProvider.location.topRight.y` | number |  |
| `fields.servicesYouMayNeedSpecialtyDrugsInNetworkProvider.type` | string |  |
| `fields.servicesYouMayNeedSpecialtyDrugsInNetworkProvider.value` | string |  |
| `fields.servicesYouMayNeedSpecialtyDrugsOutOfNetworkProvider.confidence` | number |  |
| `fields.servicesYouMayNeedSpecialtyDrugsOutOfNetworkProvider.key` | string |  |
| `fields.servicesYouMayNeedSpecialtyDrugsOutOfNetworkProvider.location.bottomLeft.x` | number |  |
| `fields.servicesYouMayNeedSpecialtyDrugsOutOfNetworkProvider.location.bottomLeft.y` | number |  |
| `fields.servicesYouMayNeedSpecialtyDrugsOutOfNetworkProvider.location.bottomRight.x` | number |  |
| `fields.servicesYouMayNeedSpecialtyDrugsOutOfNetworkProvider.location.bottomRight.y` | number |  |
| `fields.servicesYouMayNeedSpecialtyDrugsOutOfNetworkProvider.location.pageNumber` | number |  |
| `fields.servicesYouMayNeedSpecialtyDrugsOutOfNetworkProvider.location.topLeft.x` | number |  |
| `fields.servicesYouMayNeedSpecialtyDrugsOutOfNetworkProvider.location.topLeft.y` | number |  |
| `fields.servicesYouMayNeedSpecialtyDrugsOutOfNetworkProvider.location.topRight.x` | number |  |
| `fields.servicesYouMayNeedSpecialtyDrugsOutOfNetworkProvider.location.topRight.y` | number |  |
| `fields.servicesYouMayNeedSpecialtyDrugsOutOfNetworkProvider.type` | string |  |
| `fields.servicesYouMayNeedSpecialtyDrugsOutOfNetworkProvider.value` | string |  |
| `fields.servicesYouMayNeedUrgentCareInNetworkProvider.confidence` | number |  |
| `fields.servicesYouMayNeedUrgentCareInNetworkProvider.key` | string |  |
| `fields.servicesYouMayNeedUrgentCareInNetworkProvider.location.bottomLeft.x` | number |  |
| `fields.servicesYouMayNeedUrgentCareInNetworkProvider.location.bottomLeft.y` | number |  |
| `fields.servicesYouMayNeedUrgentCareInNetworkProvider.location.bottomRight.x` | number |  |
| `fields.servicesYouMayNeedUrgentCareInNetworkProvider.location.bottomRight.y` | number |  |
| `fields.servicesYouMayNeedUrgentCareInNetworkProvider.location.pageNumber` | number |  |
| `fields.servicesYouMayNeedUrgentCareInNetworkProvider.location.topLeft.x` | number |  |
| `fields.servicesYouMayNeedUrgentCareInNetworkProvider.location.topLeft.y` | number |  |
| `fields.servicesYouMayNeedUrgentCareInNetworkProvider.location.topRight.x` | number |  |
| `fields.servicesYouMayNeedUrgentCareInNetworkProvider.location.topRight.y` | number |  |
| `fields.servicesYouMayNeedUrgentCareInNetworkProvider.type` | string |  |
| `fields.servicesYouMayNeedUrgentCareInNetworkProvider.value` | string |  |
| `fields.servicesYouMayNeedUrgentCareOutOfNetworkProvider.confidence` | number |  |
| `fields.servicesYouMayNeedUrgentCareOutOfNetworkProvider.key` | string |  |
| `fields.servicesYouMayNeedUrgentCareOutOfNetworkProvider.location.bottomLeft.x` | number |  |
| `fields.servicesYouMayNeedUrgentCareOutOfNetworkProvider.location.bottomLeft.y` | number |  |
| `fields.servicesYouMayNeedUrgentCareOutOfNetworkProvider.location.bottomRight.x` | number |  |
| `fields.servicesYouMayNeedUrgentCareOutOfNetworkProvider.location.bottomRight.y` | number |  |
| `fields.servicesYouMayNeedUrgentCareOutOfNetworkProvider.location.pageNumber` | number |  |
| `fields.servicesYouMayNeedUrgentCareOutOfNetworkProvider.location.topLeft.x` | number |  |
| `fields.servicesYouMayNeedUrgentCareOutOfNetworkProvider.location.topLeft.y` | number |  |
| `fields.servicesYouMayNeedUrgentCareOutOfNetworkProvider.location.topRight.x` | number |  |
| `fields.servicesYouMayNeedUrgentCareOutOfNetworkProvider.location.topRight.y` | number |  |
| `fields.servicesYouMayNeedUrgentCareOutOfNetworkProvider.type` | string |  |
| `fields.servicesYouMayNeedUrgentCareOutOfNetworkProvider.value` | string |  |
| `model.confidence` | number |  |
| `model.isValid` | boolean |  |
| `model.name` | string |  |
| `model.shape` | string |  |
| `model.type` | string |  |
| `ocr` | string |  |
| `status` | string |  |
| `uuid` | string |  |

## Native endpoint

Through the native Base64.ai API, this operation is `POST /api/scan` (base URL `https://base64.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/scan-document-under-page-count.md) for the provider-specific parameters and requirements.

