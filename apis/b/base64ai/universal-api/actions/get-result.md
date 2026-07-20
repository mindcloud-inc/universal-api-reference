# Base64.ai: Get Result

Retrieves a specific result from Base64.ai.

```
GET https://connect.mindcloud.co/v1/universal/base64ai/latest/actions/get-result
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Base64.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/base64ai/latest/actions/get-result?connectionId=$CONNECTION_ID&resultUuid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "resultUuid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/base64ai/latest/actions/get-result?${params}`, {
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
| `resultUuid` | string | yes | Base64.ai result UUID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "fileName": "Ava Chen",
      "hitlStatus": "string",
      "linkedResults": [
        "https://example.com"
      ],
      "result": [
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
      "reviewedBy": [
        {}
      ],
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `fileName` | string |  |
| `hitlStatus` | string |  |
| `linkedResults[]` | string |  |
| `result[].features.creditsSpent` | number |  |
| `result[].features.dom.box.bottom` | number |  |
| `result[].features.dom.box.height` | number |  |
| `result[].features.dom.box.left` | number |  |
| `result[].features.dom.box.pageNumber` | object |  |
| `result[].features.dom.box.right` | number |  |
| `result[].features.dom.box.top` | number |  |
| `result[].features.dom.box.width` | number |  |
| `result[].features.dom.confidence` | number |  |
| `result[].features.dom.pages[].blocks[].box.bottom` | number |  |
| `result[].features.dom.pages[].blocks[].box.height` | number |  |
| `result[].features.dom.pages[].blocks[].box.left` | number |  |
| `result[].features.dom.pages[].blocks[].box.pageNumber` | number |  |
| `result[].features.dom.pages[].blocks[].box.right` | number |  |
| `result[].features.dom.pages[].blocks[].box.top` | number |  |
| `result[].features.dom.pages[].blocks[].box.width` | number |  |
| `result[].features.dom.pages[].blocks[].confidence` | number |  |
| `result[].features.dom.pages[].blocks[].lines[].box.bottom` | number |  |
| `result[].features.dom.pages[].blocks[].lines[].box.height` | number |  |
| `result[].features.dom.pages[].blocks[].lines[].box.left` | number |  |
| `result[].features.dom.pages[].blocks[].lines[].box.pageNumber` | number |  |
| `result[].features.dom.pages[].blocks[].lines[].box.right` | number |  |
| `result[].features.dom.pages[].blocks[].lines[].box.top` | number |  |
| `result[].features.dom.pages[].blocks[].lines[].box.width` | number |  |
| `result[].features.dom.pages[].blocks[].lines[].confidence` | number |  |
| `result[].features.dom.pages[].blocks[].lines[].location.bottomLeft.x` | number |  |
| `result[].features.dom.pages[].blocks[].lines[].location.bottomLeft.y` | number |  |
| `result[].features.dom.pages[].blocks[].lines[].location.bottomRight.x` | number |  |
| `result[].features.dom.pages[].blocks[].lines[].location.bottomRight.y` | number |  |
| `result[].features.dom.pages[].blocks[].lines[].location.pageNumber` | number |  |
| `result[].features.dom.pages[].blocks[].lines[].location.topLeft.x` | number |  |
| `result[].features.dom.pages[].blocks[].lines[].location.topLeft.y` | number |  |
| `result[].features.dom.pages[].blocks[].lines[].location.topRight.x` | number |  |
| `result[].features.dom.pages[].blocks[].lines[].location.topRight.y` | number |  |
| `result[].features.dom.pages[].blocks[].lines[].text` | string |  |
| `result[].features.dom.pages[].blocks[].lines[].words[].box.bottom` | number |  |
| `result[].features.dom.pages[].blocks[].lines[].words[].box.height` | number |  |
| `result[].features.dom.pages[].blocks[].lines[].words[].box.left` | number |  |
| `result[].features.dom.pages[].blocks[].lines[].words[].box.pageNumber` | number |  |
| `result[].features.dom.pages[].blocks[].lines[].words[].box.right` | number |  |
| `result[].features.dom.pages[].blocks[].lines[].words[].box.top` | number |  |
| `result[].features.dom.pages[].blocks[].lines[].words[].box.width` | number |  |
| `result[].features.dom.pages[].blocks[].lines[].words[].confidence` | number |  |
| `result[].features.dom.pages[].blocks[].lines[].words[].location.bottomLeft.x` | number |  |
| `result[].features.dom.pages[].blocks[].lines[].words[].location.bottomLeft.y` | number |  |
| `result[].features.dom.pages[].blocks[].lines[].words[].location.bottomRight.x` | number |  |
| `result[].features.dom.pages[].blocks[].lines[].words[].location.bottomRight.y` | number |  |
| `result[].features.dom.pages[].blocks[].lines[].words[].location.pageNumber` | number |  |
| `result[].features.dom.pages[].blocks[].lines[].words[].location.topLeft.x` | number |  |
| `result[].features.dom.pages[].blocks[].lines[].words[].location.topLeft.y` | number |  |
| `result[].features.dom.pages[].blocks[].lines[].words[].location.topRight.x` | number |  |
| `result[].features.dom.pages[].blocks[].lines[].words[].location.topRight.y` | number |  |
| `result[].features.dom.pages[].blocks[].lines[].words[].text` | string |  |
| `result[].features.dom.pages[].blocks[].location.bottomLeft.x` | number |  |
| `result[].features.dom.pages[].blocks[].location.bottomLeft.y` | number |  |
| `result[].features.dom.pages[].blocks[].location.bottomRight.x` | number |  |
| `result[].features.dom.pages[].blocks[].location.bottomRight.y` | number |  |
| `result[].features.dom.pages[].blocks[].location.pageNumber` | number |  |
| `result[].features.dom.pages[].blocks[].location.topLeft.x` | number |  |
| `result[].features.dom.pages[].blocks[].location.topLeft.y` | number |  |
| `result[].features.dom.pages[].blocks[].location.topRight.x` | number |  |
| `result[].features.dom.pages[].blocks[].location.topRight.y` | number |  |
| `result[].features.dom.pages[].blocks[].text` | string |  |
| `result[].features.dom.pages[].box.bottom` | number |  |
| `result[].features.dom.pages[].box.height` | number |  |
| `result[].features.dom.pages[].box.left` | number |  |
| `result[].features.dom.pages[].box.pageNumber` | number |  |
| `result[].features.dom.pages[].box.right` | number |  |
| `result[].features.dom.pages[].box.top` | number |  |
| `result[].features.dom.pages[].box.width` | number |  |
| `result[].features.dom.pages[].confidence` | number |  |
| `result[].features.dom.pages[].location.bottomLeft.x` | number |  |
| `result[].features.dom.pages[].location.bottomLeft.y` | number |  |
| `result[].features.dom.pages[].location.bottomRight.x` | number |  |
| `result[].features.dom.pages[].location.bottomRight.y` | number |  |
| `result[].features.dom.pages[].location.pageNumber` | number |  |
| `result[].features.dom.pages[].location.topLeft.x` | number |  |
| `result[].features.dom.pages[].location.topLeft.y` | number |  |
| `result[].features.dom.pages[].location.topRight.x` | number |  |
| `result[].features.dom.pages[].location.topRight.y` | number |  |
| `result[].features.dom.pages[].properties.dpiX` | number |  |
| `result[].features.dom.pages[].properties.dpiY` | number |  |
| `result[].features.dom.pages[].properties.height` | number |  |
| `result[].features.dom.pages[].properties.mimeType` | string |  |
| `result[].features.dom.pages[].properties.normalizedHeight` | number |  |
| `result[].features.dom.pages[].properties.normalizedWidth` | number |  |
| `result[].features.dom.pages[].properties.rotationAngle` | number |  |
| `result[].features.dom.pages[].properties.width` | number |  |
| `result[].features.dom.pages[].tables[].blocks.after.box.bottom` | number |  |
| `result[].features.dom.pages[].tables[].blocks.after.box.height` | number |  |
| `result[].features.dom.pages[].tables[].blocks.after.box.left` | number |  |
| `result[].features.dom.pages[].tables[].blocks.after.box.pageNumber` | number |  |
| `result[].features.dom.pages[].tables[].blocks.after.box.right` | number |  |
| `result[].features.dom.pages[].tables[].blocks.after.box.top` | number |  |
| `result[].features.dom.pages[].tables[].blocks.after.box.width` | number |  |
| `result[].features.dom.pages[].tables[].blocks.after.confidence` | number |  |
| `result[].features.dom.pages[].tables[].blocks.after.lines[].box.bottom` | number |  |
| `result[].features.dom.pages[].tables[].blocks.after.lines[].box.height` | number |  |
| `result[].features.dom.pages[].tables[].blocks.after.lines[].box.left` | number |  |
| `result[].features.dom.pages[].tables[].blocks.after.lines[].box.pageNumber` | number |  |
| `result[].features.dom.pages[].tables[].blocks.after.lines[].box.right` | number |  |
| `result[].features.dom.pages[].tables[].blocks.after.lines[].box.top` | number |  |
| `result[].features.dom.pages[].tables[].blocks.after.lines[].box.width` | number |  |
| `result[].features.dom.pages[].tables[].blocks.after.lines[].confidence` | number |  |
| `result[].features.dom.pages[].tables[].blocks.after.lines[].location.bottomLeft.x` | number |  |
| `result[].features.dom.pages[].tables[].blocks.after.lines[].location.bottomLeft.y` | number |  |
| `result[].features.dom.pages[].tables[].blocks.after.lines[].location.bottomRight.x` | number |  |
| `result[].features.dom.pages[].tables[].blocks.after.lines[].location.bottomRight.y` | number |  |
| `result[].features.dom.pages[].tables[].blocks.after.lines[].location.pageNumber` | number |  |
| `result[].features.dom.pages[].tables[].blocks.after.lines[].location.topLeft.x` | number |  |
| `result[].features.dom.pages[].tables[].blocks.after.lines[].location.topLeft.y` | number |  |
| `result[].features.dom.pages[].tables[].blocks.after.lines[].location.topRight.x` | number |  |
| `result[].features.dom.pages[].tables[].blocks.after.lines[].location.topRight.y` | number |  |
| `result[].features.dom.pages[].tables[].blocks.after.lines[].text` | string |  |
| `result[].features.dom.pages[].tables[].blocks.after.lines[].words[].box.bottom` | number |  |
| `result[].features.dom.pages[].tables[].blocks.after.lines[].words[].box.height` | number |  |
| `result[].features.dom.pages[].tables[].blocks.after.lines[].words[].box.left` | number |  |
| `result[].features.dom.pages[].tables[].blocks.after.lines[].words[].box.pageNumber` | number |  |
| `result[].features.dom.pages[].tables[].blocks.after.lines[].words[].box.right` | number |  |
| `result[].features.dom.pages[].tables[].blocks.after.lines[].words[].box.top` | number |  |
| `result[].features.dom.pages[].tables[].blocks.after.lines[].words[].box.width` | number |  |
| `result[].features.dom.pages[].tables[].blocks.after.lines[].words[].confidence` | number |  |
| `result[].features.dom.pages[].tables[].blocks.after.lines[].words[].location.bottomLeft.x` | number |  |
| `result[].features.dom.pages[].tables[].blocks.after.lines[].words[].location.bottomLeft.y` | number |  |
| `result[].features.dom.pages[].tables[].blocks.after.lines[].words[].location.bottomRight.x` | number |  |
| `result[].features.dom.pages[].tables[].blocks.after.lines[].words[].location.bottomRight.y` | number |  |
| `result[].features.dom.pages[].tables[].blocks.after.lines[].words[].location.pageNumber` | number |  |
| `result[].features.dom.pages[].tables[].blocks.after.lines[].words[].location.topLeft.x` | number |  |
| `result[].features.dom.pages[].tables[].blocks.after.lines[].words[].location.topLeft.y` | number |  |
| `result[].features.dom.pages[].tables[].blocks.after.lines[].words[].location.topRight.x` | number |  |
| `result[].features.dom.pages[].tables[].blocks.after.lines[].words[].location.topRight.y` | number |  |
| `result[].features.dom.pages[].tables[].blocks.after.lines[].words[].text` | string |  |
| `result[].features.dom.pages[].tables[].blocks.after.location.bottomLeft.x` | number |  |
| `result[].features.dom.pages[].tables[].blocks.after.location.bottomLeft.y` | number |  |
| `result[].features.dom.pages[].tables[].blocks.after.location.bottomRight.x` | number |  |
| `result[].features.dom.pages[].tables[].blocks.after.location.bottomRight.y` | number |  |
| `result[].features.dom.pages[].tables[].blocks.after.location.pageNumber` | number |  |
| `result[].features.dom.pages[].tables[].blocks.after.location.topLeft.x` | number |  |
| `result[].features.dom.pages[].tables[].blocks.after.location.topLeft.y` | number |  |
| `result[].features.dom.pages[].tables[].blocks.after.location.topRight.x` | number |  |
| `result[].features.dom.pages[].tables[].blocks.after.location.topRight.y` | number |  |
| `result[].features.dom.pages[].tables[].blocks.after.text` | string |  |
| `result[].features.dom.pages[].tables[].blocks.before.box.bottom` | number |  |
| `result[].features.dom.pages[].tables[].blocks.before.box.height` | number |  |
| `result[].features.dom.pages[].tables[].blocks.before.box.left` | number |  |
| `result[].features.dom.pages[].tables[].blocks.before.box.pageNumber` | number |  |
| `result[].features.dom.pages[].tables[].blocks.before.box.right` | number |  |
| `result[].features.dom.pages[].tables[].blocks.before.box.top` | number |  |
| `result[].features.dom.pages[].tables[].blocks.before.box.width` | number |  |
| `result[].features.dom.pages[].tables[].blocks.before.confidence` | number |  |
| `result[].features.dom.pages[].tables[].blocks.before.lines[].box.bottom` | number |  |
| `result[].features.dom.pages[].tables[].blocks.before.lines[].box.height` | number |  |
| `result[].features.dom.pages[].tables[].blocks.before.lines[].box.left` | number |  |
| `result[].features.dom.pages[].tables[].blocks.before.lines[].box.pageNumber` | number |  |
| `result[].features.dom.pages[].tables[].blocks.before.lines[].box.right` | number |  |
| `result[].features.dom.pages[].tables[].blocks.before.lines[].box.top` | number |  |
| `result[].features.dom.pages[].tables[].blocks.before.lines[].box.width` | number |  |
| `result[].features.dom.pages[].tables[].blocks.before.lines[].confidence` | number |  |
| `result[].features.dom.pages[].tables[].blocks.before.lines[].location.bottomLeft.x` | number |  |
| `result[].features.dom.pages[].tables[].blocks.before.lines[].location.bottomLeft.y` | number |  |
| `result[].features.dom.pages[].tables[].blocks.before.lines[].location.bottomRight.x` | number |  |
| `result[].features.dom.pages[].tables[].blocks.before.lines[].location.bottomRight.y` | number |  |
| `result[].features.dom.pages[].tables[].blocks.before.lines[].location.pageNumber` | number |  |
| `result[].features.dom.pages[].tables[].blocks.before.lines[].location.topLeft.x` | number |  |
| `result[].features.dom.pages[].tables[].blocks.before.lines[].location.topLeft.y` | number |  |
| `result[].features.dom.pages[].tables[].blocks.before.lines[].location.topRight.x` | number |  |
| `result[].features.dom.pages[].tables[].blocks.before.lines[].location.topRight.y` | number |  |
| `result[].features.dom.pages[].tables[].blocks.before.lines[].text` | string |  |
| `result[].features.dom.pages[].tables[].blocks.before.lines[].words[].box.bottom` | number |  |
| `result[].features.dom.pages[].tables[].blocks.before.lines[].words[].box.height` | number |  |
| `result[].features.dom.pages[].tables[].blocks.before.lines[].words[].box.left` | number |  |
| `result[].features.dom.pages[].tables[].blocks.before.lines[].words[].box.pageNumber` | number |  |
| `result[].features.dom.pages[].tables[].blocks.before.lines[].words[].box.right` | number |  |
| `result[].features.dom.pages[].tables[].blocks.before.lines[].words[].box.top` | number |  |
| `result[].features.dom.pages[].tables[].blocks.before.lines[].words[].box.width` | number |  |
| `result[].features.dom.pages[].tables[].blocks.before.lines[].words[].confidence` | number |  |
| `result[].features.dom.pages[].tables[].blocks.before.lines[].words[].location.bottomLeft.x` | number |  |
| `result[].features.dom.pages[].tables[].blocks.before.lines[].words[].location.bottomLeft.y` | number |  |
| `result[].features.dom.pages[].tables[].blocks.before.lines[].words[].location.bottomRight.x` | number |  |
| `result[].features.dom.pages[].tables[].blocks.before.lines[].words[].location.bottomRight.y` | number |  |
| `result[].features.dom.pages[].tables[].blocks.before.lines[].words[].location.pageNumber` | number |  |
| `result[].features.dom.pages[].tables[].blocks.before.lines[].words[].location.topLeft.x` | number |  |
| `result[].features.dom.pages[].tables[].blocks.before.lines[].words[].location.topLeft.y` | number |  |
| `result[].features.dom.pages[].tables[].blocks.before.lines[].words[].location.topRight.x` | number |  |
| `result[].features.dom.pages[].tables[].blocks.before.lines[].words[].location.topRight.y` | number |  |
| `result[].features.dom.pages[].tables[].blocks.before.lines[].words[].text` | string |  |
| `result[].features.dom.pages[].tables[].blocks.before.location.bottomLeft.x` | number |  |
| `result[].features.dom.pages[].tables[].blocks.before.location.bottomLeft.y` | number |  |
| `result[].features.dom.pages[].tables[].blocks.before.location.bottomRight.x` | number |  |
| `result[].features.dom.pages[].tables[].blocks.before.location.bottomRight.y` | number |  |
| `result[].features.dom.pages[].tables[].blocks.before.location.pageNumber` | number |  |
| `result[].features.dom.pages[].tables[].blocks.before.location.topLeft.x` | number |  |
| `result[].features.dom.pages[].tables[].blocks.before.location.topLeft.y` | number |  |
| `result[].features.dom.pages[].tables[].blocks.before.location.topRight.x` | number |  |
| `result[].features.dom.pages[].tables[].blocks.before.location.topRight.y` | number |  |
| `result[].features.dom.pages[].tables[].blocks.before.text` | string |  |
| `result[].features.dom.pages[].tables[].box.bottom` | number |  |
| `result[].features.dom.pages[].tables[].box.height` | number |  |
| `result[].features.dom.pages[].tables[].box.left` | number |  |
| `result[].features.dom.pages[].tables[].box.pageNumber` | number |  |
| `result[].features.dom.pages[].tables[].box.right` | number |  |
| `result[].features.dom.pages[].tables[].box.top` | number |  |
| `result[].features.dom.pages[].tables[].box.width` | number |  |
| `result[].features.dom.pages[].tables[].rows[].cells[].confidence` | number |  |
| `result[].features.dom.pages[].tables[].rows[].cells[].text` | string |  |
| `result[].features.dom.pages[].tables[].rows[].isHeader` | boolean |  |
| `result[].features.dom.pages[].tables[].rows[].text` | string |  |
| `result[].features.dom.pages[].tables[].text` | string |  |
| `result[].features.dom.pages[].tables[].title` | string |  |
| `result[].features.dom.pages[].text` | string |  |
| `result[].features.dom.text` | string |  |
| `result[].features.fraud.indicators[].category` | string |  |
| `result[].features.fraud.indicators[].confidence` | string |  |
| `result[].features.fraud.indicators[].description` | string |  |
| `result[].features.fraud.indicators[].evidences[].ocr` | string |  |
| `result[].features.fraud.indicators[].name` | string |  |
| `result[].features.fraud.indicators[].risk` | string |  |
| `result[].features.fraud.risk` | string |  |
| `result[].features.properties.createdAt` | date |  |
| `result[].features.properties.documentPageCount` | number |  |
| `result[].features.properties.dpiX` | number |  |
| `result[].features.properties.dpiY` | number |  |
| `result[].features.properties.flowID` | string |  |
| `result[].features.properties.height` | number |  |
| `result[].features.properties.isEditable` | boolean |  |
| `result[].features.properties.isGlareFree` | boolean |  |
| `result[].features.properties.isInFocus` | boolean |  |
| `result[].features.properties.isSelectable` | boolean |  |
| `result[].features.properties.mimeType` | string |  |
| `result[].features.properties.originalFileName` | string |  |
| `result[].features.properties.pageCount` | number |  |
| `result[].features.properties.rotationAngle` | number |  |
| `result[].features.properties.startPage` | number |  |
| `result[].features.properties.width` | number |  |
| `result[].features.tables[]` | object |  |
| `result[].fields.benefitHeader.confidence` | number |  |
| `result[].fields.benefitHeader.key` | string |  |
| `result[].fields.benefitHeader.location.bottomLeft.x` | number |  |
| `result[].fields.benefitHeader.location.bottomLeft.y` | number |  |
| `result[].fields.benefitHeader.location.bottomRight.x` | number |  |
| `result[].fields.benefitHeader.location.bottomRight.y` | number |  |
| `result[].fields.benefitHeader.location.pageNumber` | number |  |
| `result[].fields.benefitHeader.location.topLeft.x` | number |  |
| `result[].fields.benefitHeader.location.topLeft.y` | number |  |
| `result[].fields.benefitHeader.location.topRight.x` | number |  |
| `result[].fields.benefitHeader.location.topRight.y` | number |  |
| `result[].fields.benefitHeader.value` | string |  |
| `result[].fields.carrierName.confidence` | number |  |
| `result[].fields.carrierName.key` | string |  |
| `result[].fields.carrierName.location.bottomLeft.x` | number |  |
| `result[].fields.carrierName.location.bottomLeft.y` | number |  |
| `result[].fields.carrierName.location.bottomRight.x` | number |  |
| `result[].fields.carrierName.location.bottomRight.y` | number |  |
| `result[].fields.carrierName.location.pageNumber` | number |  |
| `result[].fields.carrierName.location.topLeft.x` | number |  |
| `result[].fields.carrierName.location.topLeft.y` | number |  |
| `result[].fields.carrierName.location.topRight.x` | number |  |
| `result[].fields.carrierName.location.topRight.y` | number |  |
| `result[].fields.carrierName.value` | string |  |
| `result[].fields.coverageEnd.confidence` | number |  |
| `result[].fields.coverageEnd.isValid` | boolean |  |
| `result[].fields.coverageEnd.key` | string |  |
| `result[].fields.coverageEnd.location.bottomLeft.x` | number |  |
| `result[].fields.coverageEnd.location.bottomLeft.y` | number |  |
| `result[].fields.coverageEnd.location.bottomRight.x` | number |  |
| `result[].fields.coverageEnd.location.bottomRight.y` | number |  |
| `result[].fields.coverageEnd.location.pageNumber` | number |  |
| `result[].fields.coverageEnd.location.topLeft.x` | number |  |
| `result[].fields.coverageEnd.location.topLeft.y` | number |  |
| `result[].fields.coverageEnd.location.topRight.x` | number |  |
| `result[].fields.coverageEnd.location.topRight.y` | number |  |
| `result[].fields.coverageEnd.ocrText` | string |  |
| `result[].fields.coverageEnd.type` | string |  |
| `result[].fields.coverageEnd.value` | string |  |
| `result[].fields.coverageFor.confidence` | number |  |
| `result[].fields.coverageFor.key` | string |  |
| `result[].fields.coverageFor.location.bottomLeft.x` | number |  |
| `result[].fields.coverageFor.location.bottomLeft.y` | number |  |
| `result[].fields.coverageFor.location.bottomRight.x` | number |  |
| `result[].fields.coverageFor.location.bottomRight.y` | number |  |
| `result[].fields.coverageFor.location.pageNumber` | number |  |
| `result[].fields.coverageFor.location.topLeft.x` | number |  |
| `result[].fields.coverageFor.location.topLeft.y` | number |  |
| `result[].fields.coverageFor.location.topRight.x` | number |  |
| `result[].fields.coverageFor.location.topRight.y` | number |  |
| `result[].fields.coverageFor.ocrText` | string |  |
| `result[].fields.coverageFor.value` | string |  |
| `result[].fields.coverageStart.confidence` | number |  |
| `result[].fields.coverageStart.isValid` | boolean |  |
| `result[].fields.coverageStart.key` | string |  |
| `result[].fields.coverageStart.location.bottomLeft.x` | number |  |
| `result[].fields.coverageStart.location.bottomLeft.y` | number |  |
| `result[].fields.coverageStart.location.bottomRight.x` | number |  |
| `result[].fields.coverageStart.location.bottomRight.y` | number |  |
| `result[].fields.coverageStart.location.pageNumber` | number |  |
| `result[].fields.coverageStart.location.topLeft.x` | number |  |
| `result[].fields.coverageStart.location.topLeft.y` | number |  |
| `result[].fields.coverageStart.location.topRight.x` | number |  |
| `result[].fields.coverageStart.location.topRight.y` | number |  |
| `result[].fields.coverageStart.ocrText` | string |  |
| `result[].fields.coverageStart.type` | string |  |
| `result[].fields.coverageStart.value` | string |  |
| `result[].fields.embeddedFamilyDeductible.confidence` | number |  |
| `result[].fields.embeddedFamilyDeductible.key` | string |  |
| `result[].fields.embeddedFamilyDeductible.type` | string |  |
| `result[].fields.embeddedFamilyDeductible.value` | string |  |
| `result[].fields.familyDeductibleInNetworkProvider.confidence` | number |  |
| `result[].fields.familyDeductibleInNetworkProvider.key` | string |  |
| `result[].fields.familyDeductibleInNetworkProvider.location.bottomLeft.x` | number |  |
| `result[].fields.familyDeductibleInNetworkProvider.location.bottomLeft.y` | number |  |
| `result[].fields.familyDeductibleInNetworkProvider.location.bottomRight.x` | number |  |
| `result[].fields.familyDeductibleInNetworkProvider.location.bottomRight.y` | number |  |
| `result[].fields.familyDeductibleInNetworkProvider.location.pageNumber` | number |  |
| `result[].fields.familyDeductibleInNetworkProvider.location.topLeft.x` | number |  |
| `result[].fields.familyDeductibleInNetworkProvider.location.topLeft.y` | number |  |
| `result[].fields.familyDeductibleInNetworkProvider.location.topRight.x` | number |  |
| `result[].fields.familyDeductibleInNetworkProvider.location.topRight.y` | number |  |
| `result[].fields.familyDeductibleInNetworkProvider.value` | string |  |
| `result[].fields.familyDeductibleOutOfNetworkProvider.confidence` | number |  |
| `result[].fields.familyDeductibleOutOfNetworkProvider.key` | string |  |
| `result[].fields.familyDeductibleOutOfNetworkProvider.location.bottomLeft.x` | number |  |
| `result[].fields.familyDeductibleOutOfNetworkProvider.location.bottomLeft.y` | number |  |
| `result[].fields.familyDeductibleOutOfNetworkProvider.location.bottomRight.x` | number |  |
| `result[].fields.familyDeductibleOutOfNetworkProvider.location.bottomRight.y` | number |  |
| `result[].fields.familyDeductibleOutOfNetworkProvider.location.pageNumber` | number |  |
| `result[].fields.familyDeductibleOutOfNetworkProvider.location.topLeft.x` | number |  |
| `result[].fields.familyDeductibleOutOfNetworkProvider.location.topLeft.y` | number |  |
| `result[].fields.familyDeductibleOutOfNetworkProvider.location.topRight.x` | number |  |
| `result[].fields.familyDeductibleOutOfNetworkProvider.location.topRight.y` | number |  |
| `result[].fields.familyDeductibleOutOfNetworkProvider.value` | string |  |
| `result[].fields.familyDrugDeductible.confidence` | number |  |
| `result[].fields.familyDrugDeductible.key` | string |  |
| `result[].fields.familyDrugDeductible.location.bottomLeft.x` | number |  |
| `result[].fields.familyDrugDeductible.location.bottomLeft.y` | number |  |
| `result[].fields.familyDrugDeductible.location.bottomRight.x` | number |  |
| `result[].fields.familyDrugDeductible.location.bottomRight.y` | number |  |
| `result[].fields.familyDrugDeductible.location.pageNumber` | number |  |
| `result[].fields.familyDrugDeductible.location.topLeft.x` | number |  |
| `result[].fields.familyDrugDeductible.location.topLeft.y` | number |  |
| `result[].fields.familyDrugDeductible.location.topRight.x` | number |  |
| `result[].fields.familyDrugDeductible.location.topRight.y` | number |  |
| `result[].fields.familyDrugDeductible.value` | string |  |
| `result[].fields.individualDeductibleInNetworkProvider.confidence` | number |  |
| `result[].fields.individualDeductibleInNetworkProvider.key` | string |  |
| `result[].fields.individualDeductibleInNetworkProvider.location.bottomLeft.x` | number |  |
| `result[].fields.individualDeductibleInNetworkProvider.location.bottomLeft.y` | number |  |
| `result[].fields.individualDeductibleInNetworkProvider.location.bottomRight.x` | number |  |
| `result[].fields.individualDeductibleInNetworkProvider.location.bottomRight.y` | number |  |
| `result[].fields.individualDeductibleInNetworkProvider.location.pageNumber` | number |  |
| `result[].fields.individualDeductibleInNetworkProvider.location.topLeft.x` | number |  |
| `result[].fields.individualDeductibleInNetworkProvider.location.topLeft.y` | number |  |
| `result[].fields.individualDeductibleInNetworkProvider.location.topRight.x` | number |  |
| `result[].fields.individualDeductibleInNetworkProvider.location.topRight.y` | number |  |
| `result[].fields.individualDeductibleInNetworkProvider.value` | string |  |
| `result[].fields.individualDeductibleOutOfNetworkProvider.confidence` | number |  |
| `result[].fields.individualDeductibleOutOfNetworkProvider.key` | string |  |
| `result[].fields.individualDeductibleOutOfNetworkProvider.location.bottomLeft.x` | number |  |
| `result[].fields.individualDeductibleOutOfNetworkProvider.location.bottomLeft.y` | number |  |
| `result[].fields.individualDeductibleOutOfNetworkProvider.location.bottomRight.x` | number |  |
| `result[].fields.individualDeductibleOutOfNetworkProvider.location.bottomRight.y` | number |  |
| `result[].fields.individualDeductibleOutOfNetworkProvider.location.pageNumber` | number |  |
| `result[].fields.individualDeductibleOutOfNetworkProvider.location.topLeft.x` | number |  |
| `result[].fields.individualDeductibleOutOfNetworkProvider.location.topLeft.y` | number |  |
| `result[].fields.individualDeductibleOutOfNetworkProvider.location.topRight.x` | number |  |
| `result[].fields.individualDeductibleOutOfNetworkProvider.location.topRight.y` | number |  |
| `result[].fields.individualDeductibleOutOfNetworkProvider.value` | string |  |
| `result[].fields.individualDrugDeductible.confidence` | number |  |
| `result[].fields.individualDrugDeductible.key` | string |  |
| `result[].fields.individualDrugDeductible.location.bottomLeft.x` | number |  |
| `result[].fields.individualDrugDeductible.location.bottomLeft.y` | number |  |
| `result[].fields.individualDrugDeductible.location.bottomRight.x` | number |  |
| `result[].fields.individualDrugDeductible.location.bottomRight.y` | number |  |
| `result[].fields.individualDrugDeductible.location.pageNumber` | number |  |
| `result[].fields.individualDrugDeductible.location.topLeft.x` | number |  |
| `result[].fields.individualDrugDeductible.location.topLeft.y` | number |  |
| `result[].fields.individualDrugDeductible.location.topRight.x` | number |  |
| `result[].fields.individualDrugDeductible.location.topRight.y` | number |  |
| `result[].fields.individualDrugDeductible.value` | string |  |
| `result[].fields.isGated.confidence` | number |  |
| `result[].fields.isGated.key` | string |  |
| `result[].fields.isGated.type` | string |  |
| `result[].fields.isGated.value` | string |  |
| `result[].fields.isHsaEligible.confidence` | number |  |
| `result[].fields.isHsaEligible.key` | string |  |
| `result[].fields.isHsaEligible.type` | string |  |
| `result[].fields.isHsaEligible.value` | string |  |
| `result[].fields.moopFamilyDrugInNetworkProvider.confidence` | number |  |
| `result[].fields.moopFamilyDrugInNetworkProvider.key` | string |  |
| `result[].fields.moopFamilyDrugInNetworkProvider.location.bottomLeft.x` | number |  |
| `result[].fields.moopFamilyDrugInNetworkProvider.location.bottomLeft.y` | number |  |
| `result[].fields.moopFamilyDrugInNetworkProvider.location.bottomRight.x` | number |  |
| `result[].fields.moopFamilyDrugInNetworkProvider.location.bottomRight.y` | number |  |
| `result[].fields.moopFamilyDrugInNetworkProvider.location.pageNumber` | number |  |
| `result[].fields.moopFamilyDrugInNetworkProvider.location.topLeft.x` | number |  |
| `result[].fields.moopFamilyDrugInNetworkProvider.location.topLeft.y` | number |  |
| `result[].fields.moopFamilyDrugInNetworkProvider.location.topRight.x` | number |  |
| `result[].fields.moopFamilyDrugInNetworkProvider.location.topRight.y` | number |  |
| `result[].fields.moopFamilyDrugInNetworkProvider.value` | string |  |
| `result[].fields.moopFamilyDrugOutOfNetworkProvider.confidence` | number |  |
| `result[].fields.moopFamilyDrugOutOfNetworkProvider.key` | string |  |
| `result[].fields.moopFamilyDrugOutOfNetworkProvider.location.bottomLeft.x` | number |  |
| `result[].fields.moopFamilyDrugOutOfNetworkProvider.location.bottomLeft.y` | number |  |
| `result[].fields.moopFamilyDrugOutOfNetworkProvider.location.bottomRight.x` | number |  |
| `result[].fields.moopFamilyDrugOutOfNetworkProvider.location.bottomRight.y` | number |  |
| `result[].fields.moopFamilyDrugOutOfNetworkProvider.location.pageNumber` | number |  |
| `result[].fields.moopFamilyDrugOutOfNetworkProvider.location.topLeft.x` | number |  |
| `result[].fields.moopFamilyDrugOutOfNetworkProvider.location.topLeft.y` | number |  |
| `result[].fields.moopFamilyDrugOutOfNetworkProvider.location.topRight.x` | number |  |
| `result[].fields.moopFamilyDrugOutOfNetworkProvider.location.topRight.y` | number |  |
| `result[].fields.moopFamilyDrugOutOfNetworkProvider.value` | string |  |
| `result[].fields.moopFamilyMedicalInNetworkProvider.confidence` | number |  |
| `result[].fields.moopFamilyMedicalInNetworkProvider.key` | string |  |
| `result[].fields.moopFamilyMedicalInNetworkProvider.location.bottomLeft.x` | number |  |
| `result[].fields.moopFamilyMedicalInNetworkProvider.location.bottomLeft.y` | number |  |
| `result[].fields.moopFamilyMedicalInNetworkProvider.location.bottomRight.x` | number |  |
| `result[].fields.moopFamilyMedicalInNetworkProvider.location.bottomRight.y` | number |  |
| `result[].fields.moopFamilyMedicalInNetworkProvider.location.pageNumber` | number |  |
| `result[].fields.moopFamilyMedicalInNetworkProvider.location.topLeft.x` | number |  |
| `result[].fields.moopFamilyMedicalInNetworkProvider.location.topLeft.y` | number |  |
| `result[].fields.moopFamilyMedicalInNetworkProvider.location.topRight.x` | number |  |
| `result[].fields.moopFamilyMedicalInNetworkProvider.location.topRight.y` | number |  |
| `result[].fields.moopFamilyMedicalInNetworkProvider.value` | string |  |
| `result[].fields.moopFamilyMedicalOutOfNetworkProvider.confidence` | number |  |
| `result[].fields.moopFamilyMedicalOutOfNetworkProvider.key` | string |  |
| `result[].fields.moopFamilyMedicalOutOfNetworkProvider.location.bottomLeft.x` | number |  |
| `result[].fields.moopFamilyMedicalOutOfNetworkProvider.location.bottomLeft.y` | number |  |
| `result[].fields.moopFamilyMedicalOutOfNetworkProvider.location.bottomRight.x` | number |  |
| `result[].fields.moopFamilyMedicalOutOfNetworkProvider.location.bottomRight.y` | number |  |
| `result[].fields.moopFamilyMedicalOutOfNetworkProvider.location.pageNumber` | number |  |
| `result[].fields.moopFamilyMedicalOutOfNetworkProvider.location.topLeft.x` | number |  |
| `result[].fields.moopFamilyMedicalOutOfNetworkProvider.location.topLeft.y` | number |  |
| `result[].fields.moopFamilyMedicalOutOfNetworkProvider.location.topRight.x` | number |  |
| `result[].fields.moopFamilyMedicalOutOfNetworkProvider.location.topRight.y` | number |  |
| `result[].fields.moopFamilyMedicalOutOfNetworkProvider.value` | string |  |
| `result[].fields.moopIndividualDrugInNetworkProvider.confidence` | number |  |
| `result[].fields.moopIndividualDrugInNetworkProvider.key` | string |  |
| `result[].fields.moopIndividualDrugInNetworkProvider.location.bottomLeft.x` | number |  |
| `result[].fields.moopIndividualDrugInNetworkProvider.location.bottomLeft.y` | number |  |
| `result[].fields.moopIndividualDrugInNetworkProvider.location.bottomRight.x` | number |  |
| `result[].fields.moopIndividualDrugInNetworkProvider.location.bottomRight.y` | number |  |
| `result[].fields.moopIndividualDrugInNetworkProvider.location.pageNumber` | number |  |
| `result[].fields.moopIndividualDrugInNetworkProvider.location.topLeft.x` | number |  |
| `result[].fields.moopIndividualDrugInNetworkProvider.location.topLeft.y` | number |  |
| `result[].fields.moopIndividualDrugInNetworkProvider.location.topRight.x` | number |  |
| `result[].fields.moopIndividualDrugInNetworkProvider.location.topRight.y` | number |  |
| `result[].fields.moopIndividualDrugInNetworkProvider.value` | string |  |
| `result[].fields.moopIndividualDrugOutOfNetworkProvider.confidence` | number |  |
| `result[].fields.moopIndividualDrugOutOfNetworkProvider.key` | string |  |
| `result[].fields.moopIndividualDrugOutOfNetworkProvider.location.bottomLeft.x` | number |  |
| `result[].fields.moopIndividualDrugOutOfNetworkProvider.location.bottomLeft.y` | number |  |
| `result[].fields.moopIndividualDrugOutOfNetworkProvider.location.bottomRight.x` | number |  |
| `result[].fields.moopIndividualDrugOutOfNetworkProvider.location.bottomRight.y` | number |  |
| `result[].fields.moopIndividualDrugOutOfNetworkProvider.location.pageNumber` | number |  |
| `result[].fields.moopIndividualDrugOutOfNetworkProvider.location.topLeft.x` | number |  |
| `result[].fields.moopIndividualDrugOutOfNetworkProvider.location.topLeft.y` | number |  |
| `result[].fields.moopIndividualDrugOutOfNetworkProvider.location.topRight.x` | number |  |
| `result[].fields.moopIndividualDrugOutOfNetworkProvider.location.topRight.y` | number |  |
| `result[].fields.moopIndividualDrugOutOfNetworkProvider.value` | string |  |
| `result[].fields.moopIndividualMedicalInNetworkProvider.confidence` | number |  |
| `result[].fields.moopIndividualMedicalInNetworkProvider.key` | string |  |
| `result[].fields.moopIndividualMedicalInNetworkProvider.location.bottomLeft.x` | number |  |
| `result[].fields.moopIndividualMedicalInNetworkProvider.location.bottomLeft.y` | number |  |
| `result[].fields.moopIndividualMedicalInNetworkProvider.location.bottomRight.x` | number |  |
| `result[].fields.moopIndividualMedicalInNetworkProvider.location.bottomRight.y` | number |  |
| `result[].fields.moopIndividualMedicalInNetworkProvider.location.pageNumber` | number |  |
| `result[].fields.moopIndividualMedicalInNetworkProvider.location.topLeft.x` | number |  |
| `result[].fields.moopIndividualMedicalInNetworkProvider.location.topLeft.y` | number |  |
| `result[].fields.moopIndividualMedicalInNetworkProvider.location.topRight.x` | number |  |
| `result[].fields.moopIndividualMedicalInNetworkProvider.location.topRight.y` | number |  |
| `result[].fields.moopIndividualMedicalInNetworkProvider.value` | string |  |
| `result[].fields.moopIndividualMedicalOutOfNetworkProvider.confidence` | number |  |
| `result[].fields.moopIndividualMedicalOutOfNetworkProvider.key` | string |  |
| `result[].fields.moopIndividualMedicalOutOfNetworkProvider.location.bottomLeft.x` | number |  |
| `result[].fields.moopIndividualMedicalOutOfNetworkProvider.location.bottomLeft.y` | number |  |
| `result[].fields.moopIndividualMedicalOutOfNetworkProvider.location.bottomRight.x` | number |  |
| `result[].fields.moopIndividualMedicalOutOfNetworkProvider.location.bottomRight.y` | number |  |
| `result[].fields.moopIndividualMedicalOutOfNetworkProvider.location.pageNumber` | number |  |
| `result[].fields.moopIndividualMedicalOutOfNetworkProvider.location.topLeft.x` | number |  |
| `result[].fields.moopIndividualMedicalOutOfNetworkProvider.location.topLeft.y` | number |  |
| `result[].fields.moopIndividualMedicalOutOfNetworkProvider.location.topRight.x` | number |  |
| `result[].fields.moopIndividualMedicalOutOfNetworkProvider.location.topRight.y` | number |  |
| `result[].fields.moopIndividualMedicalOutOfNetworkProvider.value` | string |  |
| `result[].fields.needReferralToSeeASpecialist.confidence` | number |  |
| `result[].fields.needReferralToSeeASpecialist.key` | string |  |
| `result[].fields.needReferralToSeeASpecialist.location.bottomLeft.x` | number |  |
| `result[].fields.needReferralToSeeASpecialist.location.bottomLeft.y` | number |  |
| `result[].fields.needReferralToSeeASpecialist.location.bottomRight.x` | number |  |
| `result[].fields.needReferralToSeeASpecialist.location.bottomRight.y` | number |  |
| `result[].fields.needReferralToSeeASpecialist.location.pageNumber` | number |  |
| `result[].fields.needReferralToSeeASpecialist.location.topLeft.x` | number |  |
| `result[].fields.needReferralToSeeASpecialist.location.topLeft.y` | number |  |
| `result[].fields.needReferralToSeeASpecialist.location.topRight.x` | number |  |
| `result[].fields.needReferralToSeeASpecialist.location.topRight.y` | number |  |
| `result[].fields.needReferralToSeeASpecialist.value` | string |  |
| `result[].fields.notIncludedInTheOutOfPocketLimit.confidence` | number |  |
| `result[].fields.notIncludedInTheOutOfPocketLimit.key` | string |  |
| `result[].fields.notIncludedInTheOutOfPocketLimit.location.bottomLeft.x` | number |  |
| `result[].fields.notIncludedInTheOutOfPocketLimit.location.bottomLeft.y` | number |  |
| `result[].fields.notIncludedInTheOutOfPocketLimit.location.bottomRight.x` | number |  |
| `result[].fields.notIncludedInTheOutOfPocketLimit.location.bottomRight.y` | number |  |
| `result[].fields.notIncludedInTheOutOfPocketLimit.location.pageNumber` | number |  |
| `result[].fields.notIncludedInTheOutOfPocketLimit.location.topLeft.x` | number |  |
| `result[].fields.notIncludedInTheOutOfPocketLimit.location.topLeft.y` | number |  |
| `result[].fields.notIncludedInTheOutOfPocketLimit.location.topRight.x` | number |  |
| `result[].fields.notIncludedInTheOutOfPocketLimit.location.topRight.y` | number |  |
| `result[].fields.notIncludedInTheOutOfPocketLimit.value` | string |  |
| `result[].fields.numberOfDeductibleTiers.confidence` | number |  |
| `result[].fields.numberOfDeductibleTiers.key` | string |  |
| `result[].fields.numberOfDeductibleTiers.value` | number |  |
| `result[].fields.numberOfMoopTiers.confidence` | number |  |
| `result[].fields.numberOfMoopTiers.key` | string |  |
| `result[].fields.numberOfMoopTiers.value` | number |  |
| `result[].fields.numberOfTiers.confidence` | number |  |
| `result[].fields.numberOfTiers.key` | string |  |
| `result[].fields.numberOfTiers.value` | number |  |
| `result[].fields.otherCoveredServicesAbortion.confidence` | number |  |
| `result[].fields.otherCoveredServicesAbortion.key` | string |  |
| `result[].fields.otherCoveredServicesAbortion.type` | string |  |
| `result[].fields.otherCoveredServicesAbortion.value` | string |  |
| `result[].fields.otherCoveredServicesAcupuncture.confidence` | number |  |
| `result[].fields.otherCoveredServicesAcupuncture.key` | string |  |
| `result[].fields.otherCoveredServicesAcupuncture.type` | string |  |
| `result[].fields.otherCoveredServicesAcupuncture.value` | string |  |
| `result[].fields.otherCoveredServicesAdultDental.confidence` | number |  |
| `result[].fields.otherCoveredServicesAdultDental.key` | string |  |
| `result[].fields.otherCoveredServicesAdultDental.type` | string |  |
| `result[].fields.otherCoveredServicesAdultDental.value` | string |  |
| `result[].fields.otherCoveredServicesBariatricSurgery.confidence` | number |  |
| `result[].fields.otherCoveredServicesBariatricSurgery.key` | string |  |
| `result[].fields.otherCoveredServicesBariatricSurgery.type` | string |  |
| `result[].fields.otherCoveredServicesBariatricSurgery.value` | string |  |
| `result[].fields.otherCoveredServicesChiropracticServices.confidence` | number |  |
| `result[].fields.otherCoveredServicesChiropracticServices.key` | string |  |
| `result[].fields.otherCoveredServicesChiropracticServices.type` | string |  |
| `result[].fields.otherCoveredServicesChiropracticServices.value` | string |  |
| `result[].fields.otherCoveredServicesHearingAids.confidence` | number |  |
| `result[].fields.otherCoveredServicesHearingAids.key` | string |  |
| `result[].fields.otherCoveredServicesHearingAids.type` | string |  |
| `result[].fields.otherCoveredServicesHearingAids.value` | string |  |
| `result[].fields.otherCoveredServicesInfertilityTreatment.confidence` | number |  |
| `result[].fields.otherCoveredServicesInfertilityTreatment.key` | string |  |
| `result[].fields.otherCoveredServicesInfertilityTreatment.type` | string |  |
| `result[].fields.otherCoveredServicesInfertilityTreatment.value` | string |  |
| `result[].fields.otherCoveredServicesPrivateDutyNursing.confidence` | number |  |
| `result[].fields.otherCoveredServicesPrivateDutyNursing.key` | string |  |
| `result[].fields.otherCoveredServicesPrivateDutyNursing.type` | string |  |
| `result[].fields.otherCoveredServicesPrivateDutyNursing.value` | string |  |
| `result[].fields.otherCoveredServicesRoutineEyeCare.confidence` | number |  |
| `result[].fields.otherCoveredServicesRoutineEyeCare.key` | string |  |
| `result[].fields.otherCoveredServicesRoutineEyeCare.type` | string |  |
| `result[].fields.otherCoveredServicesRoutineEyeCare.value` | string |  |
| `result[].fields.otherCoveredServicesWeightLossPrograms.confidence` | number |  |
| `result[].fields.otherCoveredServicesWeightLossPrograms.key` | string |  |
| `result[].fields.otherCoveredServicesWeightLossPrograms.type` | string |  |
| `result[].fields.otherCoveredServicesWeightLossPrograms.value` | string |  |
| `result[].fields.otherDeductibles.confidence` | number |  |
| `result[].fields.otherDeductibles.key` | string |  |
| `result[].fields.otherDeductibles.location.bottomLeft.x` | number |  |
| `result[].fields.otherDeductibles.location.bottomLeft.y` | number |  |
| `result[].fields.otherDeductibles.location.bottomRight.x` | number |  |
| `result[].fields.otherDeductibles.location.bottomRight.y` | number |  |
| `result[].fields.otherDeductibles.location.pageNumber` | number |  |
| `result[].fields.otherDeductibles.location.topLeft.x` | number |  |
| `result[].fields.otherDeductibles.location.topLeft.y` | number |  |
| `result[].fields.otherDeductibles.location.topRight.x` | number |  |
| `result[].fields.otherDeductibles.location.topRight.y` | number |  |
| `result[].fields.otherDeductibles.value` | string |  |
| `result[].fields.outOfPocketLimit.confidence` | number |  |
| `result[].fields.outOfPocketLimit.key` | string |  |
| `result[].fields.outOfPocketLimit.location.bottomLeft.x` | number |  |
| `result[].fields.outOfPocketLimit.location.bottomLeft.y` | number |  |
| `result[].fields.outOfPocketLimit.location.bottomRight.x` | number |  |
| `result[].fields.outOfPocketLimit.location.bottomRight.y` | number |  |
| `result[].fields.outOfPocketLimit.location.pageNumber` | number |  |
| `result[].fields.outOfPocketLimit.location.topLeft.x` | number |  |
| `result[].fields.outOfPocketLimit.location.topLeft.y` | number |  |
| `result[].fields.outOfPocketLimit.location.topRight.x` | number |  |
| `result[].fields.outOfPocketLimit.location.topRight.y` | number |  |
| `result[].fields.outOfPocketLimit.value` | string |  |
| `result[].fields.overallDeductible.confidence` | number |  |
| `result[].fields.overallDeductible.key` | string |  |
| `result[].fields.overallDeductible.location.bottomLeft.x` | number |  |
| `result[].fields.overallDeductible.location.bottomLeft.y` | number |  |
| `result[].fields.overallDeductible.location.bottomRight.x` | number |  |
| `result[].fields.overallDeductible.location.bottomRight.y` | number |  |
| `result[].fields.overallDeductible.location.pageNumber` | number |  |
| `result[].fields.overallDeductible.location.topLeft.x` | number |  |
| `result[].fields.overallDeductible.location.topLeft.y` | number |  |
| `result[].fields.overallDeductible.location.topRight.x` | number |  |
| `result[].fields.overallDeductible.location.topRight.y` | number |  |
| `result[].fields.overallDeductible.value` | string |  |
| `result[].fields.payLessWithInNetworkProvider.confidence` | number |  |
| `result[].fields.payLessWithInNetworkProvider.key` | string |  |
| `result[].fields.payLessWithInNetworkProvider.location.bottomLeft.x` | number |  |
| `result[].fields.payLessWithInNetworkProvider.location.bottomLeft.y` | number |  |
| `result[].fields.payLessWithInNetworkProvider.location.bottomRight.x` | number |  |
| `result[].fields.payLessWithInNetworkProvider.location.bottomRight.y` | number |  |
| `result[].fields.payLessWithInNetworkProvider.location.pageNumber` | number |  |
| `result[].fields.payLessWithInNetworkProvider.location.topLeft.x` | number |  |
| `result[].fields.payLessWithInNetworkProvider.location.topLeft.y` | number |  |
| `result[].fields.payLessWithInNetworkProvider.location.topRight.x` | number |  |
| `result[].fields.payLessWithInNetworkProvider.location.topRight.y` | number |  |
| `result[].fields.payLessWithInNetworkProvider.type` | string |  |
| `result[].fields.payLessWithInNetworkProvider.value` | string |  |
| `result[].fields.phoneNumber.confidence` | number |  |
| `result[].fields.phoneNumber.key` | string |  |
| `result[].fields.phoneNumber.location.bottomLeft.x` | number |  |
| `result[].fields.phoneNumber.location.bottomLeft.y` | number |  |
| `result[].fields.phoneNumber.location.bottomRight.x` | number |  |
| `result[].fields.phoneNumber.location.bottomRight.y` | number |  |
| `result[].fields.phoneNumber.location.pageNumber` | number |  |
| `result[].fields.phoneNumber.location.topLeft.x` | number |  |
| `result[].fields.phoneNumber.location.topLeft.y` | number |  |
| `result[].fields.phoneNumber.location.topRight.x` | number |  |
| `result[].fields.phoneNumber.location.topRight.y` | number |  |
| `result[].fields.phoneNumber.value` | string |  |
| `result[].fields.planName.confidence` | number |  |
| `result[].fields.planName.key` | string |  |
| `result[].fields.planName.location.bottomLeft.x` | number |  |
| `result[].fields.planName.location.bottomLeft.y` | number |  |
| `result[].fields.planName.location.bottomRight.x` | number |  |
| `result[].fields.planName.location.bottomRight.y` | number |  |
| `result[].fields.planName.location.pageNumber` | number |  |
| `result[].fields.planName.location.topLeft.x` | number |  |
| `result[].fields.planName.location.topLeft.y` | number |  |
| `result[].fields.planName.location.topRight.x` | number |  |
| `result[].fields.planName.location.topRight.y` | number |  |
| `result[].fields.planName.ocrText` | string |  |
| `result[].fields.planName.value` | string |  |
| `result[].fields.planType.confidence` | number |  |
| `result[].fields.planType.key` | string |  |
| `result[].fields.planType.location.bottomLeft.x` | number |  |
| `result[].fields.planType.location.bottomLeft.y` | number |  |
| `result[].fields.planType.location.bottomRight.x` | number |  |
| `result[].fields.planType.location.bottomRight.y` | number |  |
| `result[].fields.planType.location.pageNumber` | number |  |
| `result[].fields.planType.location.topLeft.x` | number |  |
| `result[].fields.planType.location.topLeft.y` | number |  |
| `result[].fields.planType.location.topRight.x` | number |  |
| `result[].fields.planType.location.topRight.y` | number |  |
| `result[].fields.planType.value` | string |  |
| `result[].fields.planTypeFull.confidence` | number |  |
| `result[].fields.planTypeFull.key` | string |  |
| `result[].fields.planTypeFull.location.bottomLeft.x` | number |  |
| `result[].fields.planTypeFull.location.bottomLeft.y` | number |  |
| `result[].fields.planTypeFull.location.bottomRight.x` | number |  |
| `result[].fields.planTypeFull.location.bottomRight.y` | number |  |
| `result[].fields.planTypeFull.location.pageNumber` | number |  |
| `result[].fields.planTypeFull.location.topLeft.x` | number |  |
| `result[].fields.planTypeFull.location.topLeft.y` | number |  |
| `result[].fields.planTypeFull.location.topRight.x` | number |  |
| `result[].fields.planTypeFull.location.topRight.y` | number |  |
| `result[].fields.planTypeFull.ocrText` | string |  |
| `result[].fields.planTypeFull.value` | string |  |
| `result[].fields.servicesCoveredBeforeDeductible.confidence` | number |  |
| `result[].fields.servicesCoveredBeforeDeductible.key` | string |  |
| `result[].fields.servicesCoveredBeforeDeductible.location.bottomLeft.x` | number |  |
| `result[].fields.servicesCoveredBeforeDeductible.location.bottomLeft.y` | number |  |
| `result[].fields.servicesCoveredBeforeDeductible.location.bottomRight.x` | number |  |
| `result[].fields.servicesCoveredBeforeDeductible.location.bottomRight.y` | number |  |
| `result[].fields.servicesCoveredBeforeDeductible.location.pageNumber` | number |  |
| `result[].fields.servicesCoveredBeforeDeductible.location.topLeft.x` | number |  |
| `result[].fields.servicesCoveredBeforeDeductible.location.topLeft.y` | number |  |
| `result[].fields.servicesCoveredBeforeDeductible.location.topRight.x` | number |  |
| `result[].fields.servicesCoveredBeforeDeductible.location.topRight.y` | number |  |
| `result[].fields.servicesCoveredBeforeDeductible.value` | string |  |
| `result[].fields.servicesYouMayNeedBirthFacilityInNetworkProvider.confidence` | number |  |
| `result[].fields.servicesYouMayNeedBirthFacilityInNetworkProvider.key` | string |  |
| `result[].fields.servicesYouMayNeedBirthFacilityInNetworkProvider.location.bottomLeft.x` | number |  |
| `result[].fields.servicesYouMayNeedBirthFacilityInNetworkProvider.location.bottomLeft.y` | number |  |
| `result[].fields.servicesYouMayNeedBirthFacilityInNetworkProvider.location.bottomRight.x` | number |  |
| `result[].fields.servicesYouMayNeedBirthFacilityInNetworkProvider.location.bottomRight.y` | number |  |
| `result[].fields.servicesYouMayNeedBirthFacilityInNetworkProvider.location.pageNumber` | number |  |
| `result[].fields.servicesYouMayNeedBirthFacilityInNetworkProvider.location.topLeft.x` | number |  |
| `result[].fields.servicesYouMayNeedBirthFacilityInNetworkProvider.location.topLeft.y` | number |  |
| `result[].fields.servicesYouMayNeedBirthFacilityInNetworkProvider.location.topRight.x` | number |  |
| `result[].fields.servicesYouMayNeedBirthFacilityInNetworkProvider.location.topRight.y` | number |  |
| `result[].fields.servicesYouMayNeedBirthFacilityInNetworkProvider.type` | string |  |
| `result[].fields.servicesYouMayNeedBirthFacilityInNetworkProvider.value` | string |  |
| `result[].fields.servicesYouMayNeedBirthFacilityOutOfNetworkProvider.confidence` | number |  |
| `result[].fields.servicesYouMayNeedBirthFacilityOutOfNetworkProvider.key` | string |  |
| `result[].fields.servicesYouMayNeedBirthFacilityOutOfNetworkProvider.location.bottomLeft.x` | number |  |
| `result[].fields.servicesYouMayNeedBirthFacilityOutOfNetworkProvider.location.bottomLeft.y` | number |  |
| `result[].fields.servicesYouMayNeedBirthFacilityOutOfNetworkProvider.location.bottomRight.x` | number |  |
| `result[].fields.servicesYouMayNeedBirthFacilityOutOfNetworkProvider.location.bottomRight.y` | number |  |
| `result[].fields.servicesYouMayNeedBirthFacilityOutOfNetworkProvider.location.pageNumber` | number |  |
| `result[].fields.servicesYouMayNeedBirthFacilityOutOfNetworkProvider.location.topLeft.x` | number |  |
| `result[].fields.servicesYouMayNeedBirthFacilityOutOfNetworkProvider.location.topLeft.y` | number |  |
| `result[].fields.servicesYouMayNeedBirthFacilityOutOfNetworkProvider.location.topRight.x` | number |  |
| `result[].fields.servicesYouMayNeedBirthFacilityOutOfNetworkProvider.location.topRight.y` | number |  |
| `result[].fields.servicesYouMayNeedBirthFacilityOutOfNetworkProvider.type` | string |  |
| `result[].fields.servicesYouMayNeedBirthFacilityOutOfNetworkProvider.value` | string |  |
| `result[].fields.servicesYouMayNeedBirthOfficeVisitsInNetworkProvider.confidence` | number |  |
| `result[].fields.servicesYouMayNeedBirthOfficeVisitsInNetworkProvider.key` | string |  |
| `result[].fields.servicesYouMayNeedBirthOfficeVisitsInNetworkProvider.location.bottomLeft.x` | number |  |
| `result[].fields.servicesYouMayNeedBirthOfficeVisitsInNetworkProvider.location.bottomLeft.y` | number |  |
| `result[].fields.servicesYouMayNeedBirthOfficeVisitsInNetworkProvider.location.bottomRight.x` | number |  |
| `result[].fields.servicesYouMayNeedBirthOfficeVisitsInNetworkProvider.location.bottomRight.y` | number |  |
| `result[].fields.servicesYouMayNeedBirthOfficeVisitsInNetworkProvider.location.pageNumber` | number |  |
| `result[].fields.servicesYouMayNeedBirthOfficeVisitsInNetworkProvider.location.topLeft.x` | number |  |
| `result[].fields.servicesYouMayNeedBirthOfficeVisitsInNetworkProvider.location.topLeft.y` | number |  |
| `result[].fields.servicesYouMayNeedBirthOfficeVisitsInNetworkProvider.location.topRight.x` | number |  |
| `result[].fields.servicesYouMayNeedBirthOfficeVisitsInNetworkProvider.location.topRight.y` | number |  |
| `result[].fields.servicesYouMayNeedBirthOfficeVisitsInNetworkProvider.type` | string |  |
| `result[].fields.servicesYouMayNeedBirthOfficeVisitsInNetworkProvider.value` | string |  |
| `result[].fields.servicesYouMayNeedBirthOfficeVisitsOutOfNetworkProvider.confidence` | number |  |
| `result[].fields.servicesYouMayNeedBirthOfficeVisitsOutOfNetworkProvider.key` | string |  |
| `result[].fields.servicesYouMayNeedBirthOfficeVisitsOutOfNetworkProvider.location.bottomLeft.x` | number |  |
| `result[].fields.servicesYouMayNeedBirthOfficeVisitsOutOfNetworkProvider.location.bottomLeft.y` | number |  |
| `result[].fields.servicesYouMayNeedBirthOfficeVisitsOutOfNetworkProvider.location.bottomRight.x` | number |  |
| `result[].fields.servicesYouMayNeedBirthOfficeVisitsOutOfNetworkProvider.location.bottomRight.y` | number |  |
| `result[].fields.servicesYouMayNeedBirthOfficeVisitsOutOfNetworkProvider.location.pageNumber` | number |  |
| `result[].fields.servicesYouMayNeedBirthOfficeVisitsOutOfNetworkProvider.location.topLeft.x` | number |  |
| `result[].fields.servicesYouMayNeedBirthOfficeVisitsOutOfNetworkProvider.location.topLeft.y` | number |  |
| `result[].fields.servicesYouMayNeedBirthOfficeVisitsOutOfNetworkProvider.location.topRight.x` | number |  |
| `result[].fields.servicesYouMayNeedBirthOfficeVisitsOutOfNetworkProvider.location.topRight.y` | number |  |
| `result[].fields.servicesYouMayNeedBirthOfficeVisitsOutOfNetworkProvider.type` | string |  |
| `result[].fields.servicesYouMayNeedBirthOfficeVisitsOutOfNetworkProvider.value` | string |  |
| `result[].fields.servicesYouMayNeedBirthPhysicianInNetworkProvider.confidence` | number |  |
| `result[].fields.servicesYouMayNeedBirthPhysicianInNetworkProvider.key` | string |  |
| `result[].fields.servicesYouMayNeedBirthPhysicianInNetworkProvider.location.bottomLeft.x` | number |  |
| `result[].fields.servicesYouMayNeedBirthPhysicianInNetworkProvider.location.bottomLeft.y` | number |  |
| `result[].fields.servicesYouMayNeedBirthPhysicianInNetworkProvider.location.bottomRight.x` | number |  |
| `result[].fields.servicesYouMayNeedBirthPhysicianInNetworkProvider.location.bottomRight.y` | number |  |
| `result[].fields.servicesYouMayNeedBirthPhysicianInNetworkProvider.location.pageNumber` | number |  |
| `result[].fields.servicesYouMayNeedBirthPhysicianInNetworkProvider.location.topLeft.x` | number |  |
| `result[].fields.servicesYouMayNeedBirthPhysicianInNetworkProvider.location.topLeft.y` | number |  |
| `result[].fields.servicesYouMayNeedBirthPhysicianInNetworkProvider.location.topRight.x` | number |  |
| `result[].fields.servicesYouMayNeedBirthPhysicianInNetworkProvider.location.topRight.y` | number |  |
| `result[].fields.servicesYouMayNeedBirthPhysicianInNetworkProvider.type` | string |  |
| `result[].fields.servicesYouMayNeedBirthPhysicianInNetworkProvider.value` | string |  |
| `result[].fields.servicesYouMayNeedBirthPhysicianOutOfNetworkProvider.confidence` | number |  |
| `result[].fields.servicesYouMayNeedBirthPhysicianOutOfNetworkProvider.key` | string |  |
| `result[].fields.servicesYouMayNeedBirthPhysicianOutOfNetworkProvider.location.bottomLeft.x` | number |  |
| `result[].fields.servicesYouMayNeedBirthPhysicianOutOfNetworkProvider.location.bottomLeft.y` | number |  |
| `result[].fields.servicesYouMayNeedBirthPhysicianOutOfNetworkProvider.location.bottomRight.x` | number |  |
| `result[].fields.servicesYouMayNeedBirthPhysicianOutOfNetworkProvider.location.bottomRight.y` | number |  |
| `result[].fields.servicesYouMayNeedBirthPhysicianOutOfNetworkProvider.location.pageNumber` | number |  |
| `result[].fields.servicesYouMayNeedBirthPhysicianOutOfNetworkProvider.location.topLeft.x` | number |  |
| `result[].fields.servicesYouMayNeedBirthPhysicianOutOfNetworkProvider.location.topLeft.y` | number |  |
| `result[].fields.servicesYouMayNeedBirthPhysicianOutOfNetworkProvider.location.topRight.x` | number |  |
| `result[].fields.servicesYouMayNeedBirthPhysicianOutOfNetworkProvider.location.topRight.y` | number |  |
| `result[].fields.servicesYouMayNeedBirthPhysicianOutOfNetworkProvider.type` | string |  |
| `result[].fields.servicesYouMayNeedBirthPhysicianOutOfNetworkProvider.value` | string |  |
| `result[].fields.servicesYouMayNeedChildDentalCheckupInNetworkProvider.confidence` | number |  |
| `result[].fields.servicesYouMayNeedChildDentalCheckupInNetworkProvider.key` | string |  |
| `result[].fields.servicesYouMayNeedChildDentalCheckupInNetworkProvider.location.bottomLeft.x` | number |  |
| `result[].fields.servicesYouMayNeedChildDentalCheckupInNetworkProvider.location.bottomLeft.y` | number |  |
| `result[].fields.servicesYouMayNeedChildDentalCheckupInNetworkProvider.location.bottomRight.x` | number |  |
| `result[].fields.servicesYouMayNeedChildDentalCheckupInNetworkProvider.location.bottomRight.y` | number |  |
| `result[].fields.servicesYouMayNeedChildDentalCheckupInNetworkProvider.location.pageNumber` | number |  |
| `result[].fields.servicesYouMayNeedChildDentalCheckupInNetworkProvider.location.topLeft.x` | number |  |
| `result[].fields.servicesYouMayNeedChildDentalCheckupInNetworkProvider.location.topLeft.y` | number |  |
| `result[].fields.servicesYouMayNeedChildDentalCheckupInNetworkProvider.location.topRight.x` | number |  |
| `result[].fields.servicesYouMayNeedChildDentalCheckupInNetworkProvider.location.topRight.y` | number |  |
| `result[].fields.servicesYouMayNeedChildDentalCheckupInNetworkProvider.type` | string |  |
| `result[].fields.servicesYouMayNeedChildDentalCheckupInNetworkProvider.value` | string |  |
| `result[].fields.servicesYouMayNeedChildDentalCheckupOutOfNetworkProvider.confidence` | number |  |
| `result[].fields.servicesYouMayNeedChildDentalCheckupOutOfNetworkProvider.key` | string |  |
| `result[].fields.servicesYouMayNeedChildDentalCheckupOutOfNetworkProvider.location.bottomLeft.x` | number |  |
| `result[].fields.servicesYouMayNeedChildDentalCheckupOutOfNetworkProvider.location.bottomLeft.y` | number |  |
| `result[].fields.servicesYouMayNeedChildDentalCheckupOutOfNetworkProvider.location.bottomRight.x` | number |  |
| `result[].fields.servicesYouMayNeedChildDentalCheckupOutOfNetworkProvider.location.bottomRight.y` | number |  |
| `result[].fields.servicesYouMayNeedChildDentalCheckupOutOfNetworkProvider.location.pageNumber` | number |  |
| `result[].fields.servicesYouMayNeedChildDentalCheckupOutOfNetworkProvider.location.topLeft.x` | number |  |
| `result[].fields.servicesYouMayNeedChildDentalCheckupOutOfNetworkProvider.location.topLeft.y` | number |  |
| `result[].fields.servicesYouMayNeedChildDentalCheckupOutOfNetworkProvider.location.topRight.x` | number |  |
| `result[].fields.servicesYouMayNeedChildDentalCheckupOutOfNetworkProvider.location.topRight.y` | number |  |
| `result[].fields.servicesYouMayNeedChildDentalCheckupOutOfNetworkProvider.type` | string |  |
| `result[].fields.servicesYouMayNeedChildDentalCheckupOutOfNetworkProvider.value` | string |  |
| `result[].fields.servicesYouMayNeedChildEyeExamInNetworkProvider.confidence` | number |  |
| `result[].fields.servicesYouMayNeedChildEyeExamInNetworkProvider.key` | string |  |
| `result[].fields.servicesYouMayNeedChildEyeExamInNetworkProvider.location.bottomLeft.x` | number |  |
| `result[].fields.servicesYouMayNeedChildEyeExamInNetworkProvider.location.bottomLeft.y` | number |  |
| `result[].fields.servicesYouMayNeedChildEyeExamInNetworkProvider.location.bottomRight.x` | number |  |
| `result[].fields.servicesYouMayNeedChildEyeExamInNetworkProvider.location.bottomRight.y` | number |  |
| `result[].fields.servicesYouMayNeedChildEyeExamInNetworkProvider.location.pageNumber` | number |  |
| `result[].fields.servicesYouMayNeedChildEyeExamInNetworkProvider.location.topLeft.x` | number |  |
| `result[].fields.servicesYouMayNeedChildEyeExamInNetworkProvider.location.topLeft.y` | number |  |
| `result[].fields.servicesYouMayNeedChildEyeExamInNetworkProvider.location.topRight.x` | number |  |
| `result[].fields.servicesYouMayNeedChildEyeExamInNetworkProvider.location.topRight.y` | number |  |
| `result[].fields.servicesYouMayNeedChildEyeExamInNetworkProvider.type` | string |  |
| `result[].fields.servicesYouMayNeedChildEyeExamInNetworkProvider.value` | string |  |
| `result[].fields.servicesYouMayNeedChildEyeExamOutOfNetworkProvider.confidence` | number |  |
| `result[].fields.servicesYouMayNeedChildEyeExamOutOfNetworkProvider.key` | string |  |
| `result[].fields.servicesYouMayNeedChildEyeExamOutOfNetworkProvider.location.bottomLeft.x` | number |  |
| `result[].fields.servicesYouMayNeedChildEyeExamOutOfNetworkProvider.location.bottomLeft.y` | number |  |
| `result[].fields.servicesYouMayNeedChildEyeExamOutOfNetworkProvider.location.bottomRight.x` | number |  |
| `result[].fields.servicesYouMayNeedChildEyeExamOutOfNetworkProvider.location.bottomRight.y` | number |  |
| `result[].fields.servicesYouMayNeedChildEyeExamOutOfNetworkProvider.location.pageNumber` | number |  |
| `result[].fields.servicesYouMayNeedChildEyeExamOutOfNetworkProvider.location.topLeft.x` | number |  |
| `result[].fields.servicesYouMayNeedChildEyeExamOutOfNetworkProvider.location.topLeft.y` | number |  |
| `result[].fields.servicesYouMayNeedChildEyeExamOutOfNetworkProvider.location.topRight.x` | number |  |
| `result[].fields.servicesYouMayNeedChildEyeExamOutOfNetworkProvider.location.topRight.y` | number |  |
| `result[].fields.servicesYouMayNeedChildEyeExamOutOfNetworkProvider.type` | string |  |
| `result[].fields.servicesYouMayNeedChildEyeExamOutOfNetworkProvider.value` | string |  |
| `result[].fields.servicesYouMayNeedChildGlassesInNetworkProvider.confidence` | number |  |
| `result[].fields.servicesYouMayNeedChildGlassesInNetworkProvider.key` | string |  |
| `result[].fields.servicesYouMayNeedChildGlassesInNetworkProvider.location.bottomLeft.x` | number |  |
| `result[].fields.servicesYouMayNeedChildGlassesInNetworkProvider.location.bottomLeft.y` | number |  |
| `result[].fields.servicesYouMayNeedChildGlassesInNetworkProvider.location.bottomRight.x` | number |  |
| `result[].fields.servicesYouMayNeedChildGlassesInNetworkProvider.location.bottomRight.y` | number |  |
| `result[].fields.servicesYouMayNeedChildGlassesInNetworkProvider.location.pageNumber` | number |  |
| `result[].fields.servicesYouMayNeedChildGlassesInNetworkProvider.location.topLeft.x` | number |  |
| `result[].fields.servicesYouMayNeedChildGlassesInNetworkProvider.location.topLeft.y` | number |  |
| `result[].fields.servicesYouMayNeedChildGlassesInNetworkProvider.location.topRight.x` | number |  |
| `result[].fields.servicesYouMayNeedChildGlassesInNetworkProvider.location.topRight.y` | number |  |
| `result[].fields.servicesYouMayNeedChildGlassesInNetworkProvider.type` | string |  |
| `result[].fields.servicesYouMayNeedChildGlassesInNetworkProvider.value` | string |  |
| `result[].fields.servicesYouMayNeedChildGlassesOutOfNetworkProvider.confidence` | number |  |
| `result[].fields.servicesYouMayNeedChildGlassesOutOfNetworkProvider.key` | string |  |
| `result[].fields.servicesYouMayNeedChildGlassesOutOfNetworkProvider.location.bottomLeft.x` | number |  |
| `result[].fields.servicesYouMayNeedChildGlassesOutOfNetworkProvider.location.bottomLeft.y` | number |  |
| `result[].fields.servicesYouMayNeedChildGlassesOutOfNetworkProvider.location.bottomRight.x` | number |  |
| `result[].fields.servicesYouMayNeedChildGlassesOutOfNetworkProvider.location.bottomRight.y` | number |  |
| `result[].fields.servicesYouMayNeedChildGlassesOutOfNetworkProvider.location.pageNumber` | number |  |
| `result[].fields.servicesYouMayNeedChildGlassesOutOfNetworkProvider.location.topLeft.x` | number |  |
| `result[].fields.servicesYouMayNeedChildGlassesOutOfNetworkProvider.location.topLeft.y` | number |  |
| `result[].fields.servicesYouMayNeedChildGlassesOutOfNetworkProvider.location.topRight.x` | number |  |
| `result[].fields.servicesYouMayNeedChildGlassesOutOfNetworkProvider.location.topRight.y` | number |  |
| `result[].fields.servicesYouMayNeedChildGlassesOutOfNetworkProvider.type` | string |  |
| `result[].fields.servicesYouMayNeedChildGlassesOutOfNetworkProvider.value` | string |  |
| `result[].fields.servicesYouMayNeedDiagnosticTestInNetworkProvider.confidence` | number |  |
| `result[].fields.servicesYouMayNeedDiagnosticTestInNetworkProvider.key` | string |  |
| `result[].fields.servicesYouMayNeedDiagnosticTestInNetworkProvider.location.bottomLeft.x` | number |  |
| `result[].fields.servicesYouMayNeedDiagnosticTestInNetworkProvider.location.bottomLeft.y` | number |  |
| `result[].fields.servicesYouMayNeedDiagnosticTestInNetworkProvider.location.bottomRight.x` | number |  |
| `result[].fields.servicesYouMayNeedDiagnosticTestInNetworkProvider.location.bottomRight.y` | number |  |
| `result[].fields.servicesYouMayNeedDiagnosticTestInNetworkProvider.location.pageNumber` | number |  |
| `result[].fields.servicesYouMayNeedDiagnosticTestInNetworkProvider.location.topLeft.x` | number |  |
| `result[].fields.servicesYouMayNeedDiagnosticTestInNetworkProvider.location.topLeft.y` | number |  |
| `result[].fields.servicesYouMayNeedDiagnosticTestInNetworkProvider.location.topRight.x` | number |  |
| `result[].fields.servicesYouMayNeedDiagnosticTestInNetworkProvider.location.topRight.y` | number |  |
| `result[].fields.servicesYouMayNeedDiagnosticTestInNetworkProvider.type` | string |  |
| `result[].fields.servicesYouMayNeedDiagnosticTestInNetworkProvider.value` | string |  |
| `result[].fields.servicesYouMayNeedDiagnosticTestOutOfNetworkProvider.confidence` | number |  |
| `result[].fields.servicesYouMayNeedDiagnosticTestOutOfNetworkProvider.key` | string |  |
| `result[].fields.servicesYouMayNeedDiagnosticTestOutOfNetworkProvider.location.bottomLeft.x` | number |  |
| `result[].fields.servicesYouMayNeedDiagnosticTestOutOfNetworkProvider.location.bottomLeft.y` | number |  |
| `result[].fields.servicesYouMayNeedDiagnosticTestOutOfNetworkProvider.location.bottomRight.x` | number |  |
| `result[].fields.servicesYouMayNeedDiagnosticTestOutOfNetworkProvider.location.bottomRight.y` | number |  |
| `result[].fields.servicesYouMayNeedDiagnosticTestOutOfNetworkProvider.location.pageNumber` | number |  |
| `result[].fields.servicesYouMayNeedDiagnosticTestOutOfNetworkProvider.location.topLeft.x` | number |  |
| `result[].fields.servicesYouMayNeedDiagnosticTestOutOfNetworkProvider.location.topLeft.y` | number |  |
| `result[].fields.servicesYouMayNeedDiagnosticTestOutOfNetworkProvider.location.topRight.x` | number |  |
| `result[].fields.servicesYouMayNeedDiagnosticTestOutOfNetworkProvider.location.topRight.y` | number |  |
| `result[].fields.servicesYouMayNeedDiagnosticTestOutOfNetworkProvider.type` | string |  |
| `result[].fields.servicesYouMayNeedDiagnosticTestOutOfNetworkProvider.value` | string |  |
| `result[].fields.servicesYouMayNeedDrugFormularyUrl.confidence` | number |  |
| `result[].fields.servicesYouMayNeedDrugFormularyUrl.key` | string |  |
| `result[].fields.servicesYouMayNeedDrugFormularyUrl.location.bottomLeft.x` | number |  |
| `result[].fields.servicesYouMayNeedDrugFormularyUrl.location.bottomLeft.y` | number |  |
| `result[].fields.servicesYouMayNeedDrugFormularyUrl.location.bottomRight.x` | number |  |
| `result[].fields.servicesYouMayNeedDrugFormularyUrl.location.bottomRight.y` | number |  |
| `result[].fields.servicesYouMayNeedDrugFormularyUrl.location.pageNumber` | number |  |
| `result[].fields.servicesYouMayNeedDrugFormularyUrl.location.topLeft.x` | number |  |
| `result[].fields.servicesYouMayNeedDrugFormularyUrl.location.topLeft.y` | number |  |
| `result[].fields.servicesYouMayNeedDrugFormularyUrl.location.topRight.x` | number |  |
| `result[].fields.servicesYouMayNeedDrugFormularyUrl.location.topRight.y` | number |  |
| `result[].fields.servicesYouMayNeedDrugFormularyUrl.value` | string |  |
| `result[].fields.servicesYouMayNeedDurableMedicalEquipmentInNetworkProvider.confidence` | number |  |
| `result[].fields.servicesYouMayNeedDurableMedicalEquipmentInNetworkProvider.key` | string |  |
| `result[].fields.servicesYouMayNeedDurableMedicalEquipmentInNetworkProvider.location.bottomLeft.x` | number |  |
| `result[].fields.servicesYouMayNeedDurableMedicalEquipmentInNetworkProvider.location.bottomLeft.y` | number |  |
| `result[].fields.servicesYouMayNeedDurableMedicalEquipmentInNetworkProvider.location.bottomRight.x` | number |  |
| `result[].fields.servicesYouMayNeedDurableMedicalEquipmentInNetworkProvider.location.bottomRight.y` | number |  |
| `result[].fields.servicesYouMayNeedDurableMedicalEquipmentInNetworkProvider.location.pageNumber` | number |  |
| `result[].fields.servicesYouMayNeedDurableMedicalEquipmentInNetworkProvider.location.topLeft.x` | number |  |
| `result[].fields.servicesYouMayNeedDurableMedicalEquipmentInNetworkProvider.location.topLeft.y` | number |  |
| `result[].fields.servicesYouMayNeedDurableMedicalEquipmentInNetworkProvider.location.topRight.x` | number |  |
| `result[].fields.servicesYouMayNeedDurableMedicalEquipmentInNetworkProvider.location.topRight.y` | number |  |
| `result[].fields.servicesYouMayNeedDurableMedicalEquipmentInNetworkProvider.type` | string |  |
| `result[].fields.servicesYouMayNeedDurableMedicalEquipmentInNetworkProvider.value` | string |  |
| `result[].fields.servicesYouMayNeedDurableMedicalEquipmentOutOfNetworkProvider.confidence` | number |  |
| `result[].fields.servicesYouMayNeedDurableMedicalEquipmentOutOfNetworkProvider.key` | string |  |
| `result[].fields.servicesYouMayNeedDurableMedicalEquipmentOutOfNetworkProvider.location.bottomLeft.x` | number |  |
| `result[].fields.servicesYouMayNeedDurableMedicalEquipmentOutOfNetworkProvider.location.bottomLeft.y` | number |  |
| `result[].fields.servicesYouMayNeedDurableMedicalEquipmentOutOfNetworkProvider.location.bottomRight.x` | number |  |
| `result[].fields.servicesYouMayNeedDurableMedicalEquipmentOutOfNetworkProvider.location.bottomRight.y` | number |  |
| `result[].fields.servicesYouMayNeedDurableMedicalEquipmentOutOfNetworkProvider.location.pageNumber` | number |  |
| `result[].fields.servicesYouMayNeedDurableMedicalEquipmentOutOfNetworkProvider.location.topLeft.x` | number |  |
| `result[].fields.servicesYouMayNeedDurableMedicalEquipmentOutOfNetworkProvider.location.topLeft.y` | number |  |
| `result[].fields.servicesYouMayNeedDurableMedicalEquipmentOutOfNetworkProvider.location.topRight.x` | number |  |
| `result[].fields.servicesYouMayNeedDurableMedicalEquipmentOutOfNetworkProvider.location.topRight.y` | number |  |
| `result[].fields.servicesYouMayNeedDurableMedicalEquipmentOutOfNetworkProvider.type` | string |  |
| `result[].fields.servicesYouMayNeedDurableMedicalEquipmentOutOfNetworkProvider.value` | string |  |
| `result[].fields.servicesYouMayNeedEmergencyMedicalTransportationInNetworkProvider.confidence` | number |  |
| `result[].fields.servicesYouMayNeedEmergencyMedicalTransportationInNetworkProvider.key` | string |  |
| `result[].fields.servicesYouMayNeedEmergencyMedicalTransportationInNetworkProvider.location.bottomLeft.x` | number |  |
| `result[].fields.servicesYouMayNeedEmergencyMedicalTransportationInNetworkProvider.location.bottomLeft.y` | number |  |
| `result[].fields.servicesYouMayNeedEmergencyMedicalTransportationInNetworkProvider.location.bottomRight.x` | number |  |
| `result[].fields.servicesYouMayNeedEmergencyMedicalTransportationInNetworkProvider.location.bottomRight.y` | number |  |
| `result[].fields.servicesYouMayNeedEmergencyMedicalTransportationInNetworkProvider.location.pageNumber` | number |  |
| `result[].fields.servicesYouMayNeedEmergencyMedicalTransportationInNetworkProvider.location.topLeft.x` | number |  |
| `result[].fields.servicesYouMayNeedEmergencyMedicalTransportationInNetworkProvider.location.topLeft.y` | number |  |
| `result[].fields.servicesYouMayNeedEmergencyMedicalTransportationInNetworkProvider.location.topRight.x` | number |  |
| `result[].fields.servicesYouMayNeedEmergencyMedicalTransportationInNetworkProvider.location.topRight.y` | number |  |
| `result[].fields.servicesYouMayNeedEmergencyMedicalTransportationInNetworkProvider.type` | string |  |
| `result[].fields.servicesYouMayNeedEmergencyMedicalTransportationInNetworkProvider.value` | string |  |
| `result[].fields.servicesYouMayNeedEmergencyMedicalTransportationOutOfNetworkProvider.confidence` | number |  |
| `result[].fields.servicesYouMayNeedEmergencyMedicalTransportationOutOfNetworkProvider.key` | string |  |
| `result[].fields.servicesYouMayNeedEmergencyMedicalTransportationOutOfNetworkProvider.location.bottomLeft.x` | number |  |
| `result[].fields.servicesYouMayNeedEmergencyMedicalTransportationOutOfNetworkProvider.location.bottomLeft.y` | number |  |
| `result[].fields.servicesYouMayNeedEmergencyMedicalTransportationOutOfNetworkProvider.location.bottomRight.x` | number |  |
| `result[].fields.servicesYouMayNeedEmergencyMedicalTransportationOutOfNetworkProvider.location.bottomRight.y` | number |  |
| `result[].fields.servicesYouMayNeedEmergencyMedicalTransportationOutOfNetworkProvider.location.pageNumber` | number |  |
| `result[].fields.servicesYouMayNeedEmergencyMedicalTransportationOutOfNetworkProvider.location.topLeft.x` | number |  |
| `result[].fields.servicesYouMayNeedEmergencyMedicalTransportationOutOfNetworkProvider.location.topLeft.y` | number |  |
| `result[].fields.servicesYouMayNeedEmergencyMedicalTransportationOutOfNetworkProvider.location.topRight.x` | number |  |
| `result[].fields.servicesYouMayNeedEmergencyMedicalTransportationOutOfNetworkProvider.location.topRight.y` | number |  |
| `result[].fields.servicesYouMayNeedEmergencyMedicalTransportationOutOfNetworkProvider.type` | string |  |
| `result[].fields.servicesYouMayNeedEmergencyMedicalTransportationOutOfNetworkProvider.value` | string |  |
| `result[].fields.servicesYouMayNeedEmergencyRoomCareInNetworkProvider.confidence` | number |  |
| `result[].fields.servicesYouMayNeedEmergencyRoomCareInNetworkProvider.key` | string |  |
| `result[].fields.servicesYouMayNeedEmergencyRoomCareInNetworkProvider.location.bottomLeft.x` | number |  |
| `result[].fields.servicesYouMayNeedEmergencyRoomCareInNetworkProvider.location.bottomLeft.y` | number |  |
| `result[].fields.servicesYouMayNeedEmergencyRoomCareInNetworkProvider.location.bottomRight.x` | number |  |
| `result[].fields.servicesYouMayNeedEmergencyRoomCareInNetworkProvider.location.bottomRight.y` | number |  |
| `result[].fields.servicesYouMayNeedEmergencyRoomCareInNetworkProvider.location.pageNumber` | number |  |
| `result[].fields.servicesYouMayNeedEmergencyRoomCareInNetworkProvider.location.topLeft.x` | number |  |
| `result[].fields.servicesYouMayNeedEmergencyRoomCareInNetworkProvider.location.topLeft.y` | number |  |
| `result[].fields.servicesYouMayNeedEmergencyRoomCareInNetworkProvider.location.topRight.x` | number |  |
| `result[].fields.servicesYouMayNeedEmergencyRoomCareInNetworkProvider.location.topRight.y` | number |  |
| `result[].fields.servicesYouMayNeedEmergencyRoomCareInNetworkProvider.type` | string |  |
| `result[].fields.servicesYouMayNeedEmergencyRoomCareInNetworkProvider.value` | string |  |
| `result[].fields.servicesYouMayNeedEmergencyRoomCareOutOfNetworkProvider.confidence` | number |  |
| `result[].fields.servicesYouMayNeedEmergencyRoomCareOutOfNetworkProvider.key` | string |  |
| `result[].fields.servicesYouMayNeedEmergencyRoomCareOutOfNetworkProvider.location.bottomLeft.x` | number |  |
| `result[].fields.servicesYouMayNeedEmergencyRoomCareOutOfNetworkProvider.location.bottomLeft.y` | number |  |
| `result[].fields.servicesYouMayNeedEmergencyRoomCareOutOfNetworkProvider.location.bottomRight.x` | number |  |
| `result[].fields.servicesYouMayNeedEmergencyRoomCareOutOfNetworkProvider.location.bottomRight.y` | number |  |
| `result[].fields.servicesYouMayNeedEmergencyRoomCareOutOfNetworkProvider.location.pageNumber` | number |  |
| `result[].fields.servicesYouMayNeedEmergencyRoomCareOutOfNetworkProvider.location.topLeft.x` | number |  |
| `result[].fields.servicesYouMayNeedEmergencyRoomCareOutOfNetworkProvider.location.topLeft.y` | number |  |
| `result[].fields.servicesYouMayNeedEmergencyRoomCareOutOfNetworkProvider.location.topRight.x` | number |  |
| `result[].fields.servicesYouMayNeedEmergencyRoomCareOutOfNetworkProvider.location.topRight.y` | number |  |
| `result[].fields.servicesYouMayNeedEmergencyRoomCareOutOfNetworkProvider.type` | string |  |
| `result[].fields.servicesYouMayNeedEmergencyRoomCareOutOfNetworkProvider.value` | string |  |
| `result[].fields.servicesYouMayNeedGenericDrugsInNetworkProvider.confidence` | number |  |
| `result[].fields.servicesYouMayNeedGenericDrugsInNetworkProvider.key` | string |  |
| `result[].fields.servicesYouMayNeedGenericDrugsInNetworkProvider.location.bottomLeft.x` | number |  |
| `result[].fields.servicesYouMayNeedGenericDrugsInNetworkProvider.location.bottomLeft.y` | number |  |
| `result[].fields.servicesYouMayNeedGenericDrugsInNetworkProvider.location.bottomRight.x` | number |  |
| `result[].fields.servicesYouMayNeedGenericDrugsInNetworkProvider.location.bottomRight.y` | number |  |
| `result[].fields.servicesYouMayNeedGenericDrugsInNetworkProvider.location.pageNumber` | number |  |
| `result[].fields.servicesYouMayNeedGenericDrugsInNetworkProvider.location.topLeft.x` | number |  |
| `result[].fields.servicesYouMayNeedGenericDrugsInNetworkProvider.location.topLeft.y` | number |  |
| `result[].fields.servicesYouMayNeedGenericDrugsInNetworkProvider.location.topRight.x` | number |  |
| `result[].fields.servicesYouMayNeedGenericDrugsInNetworkProvider.location.topRight.y` | number |  |
| `result[].fields.servicesYouMayNeedGenericDrugsInNetworkProvider.type` | string |  |
| `result[].fields.servicesYouMayNeedGenericDrugsInNetworkProvider.value` | string |  |
| `result[].fields.servicesYouMayNeedGenericDrugsOutOfNetworkProvider.confidence` | number |  |
| `result[].fields.servicesYouMayNeedGenericDrugsOutOfNetworkProvider.key` | string |  |
| `result[].fields.servicesYouMayNeedGenericDrugsOutOfNetworkProvider.location.bottomLeft.x` | number |  |
| `result[].fields.servicesYouMayNeedGenericDrugsOutOfNetworkProvider.location.bottomLeft.y` | number |  |
| `result[].fields.servicesYouMayNeedGenericDrugsOutOfNetworkProvider.location.bottomRight.x` | number |  |
| `result[].fields.servicesYouMayNeedGenericDrugsOutOfNetworkProvider.location.bottomRight.y` | number |  |
| `result[].fields.servicesYouMayNeedGenericDrugsOutOfNetworkProvider.location.pageNumber` | number |  |
| `result[].fields.servicesYouMayNeedGenericDrugsOutOfNetworkProvider.location.topLeft.x` | number |  |
| `result[].fields.servicesYouMayNeedGenericDrugsOutOfNetworkProvider.location.topLeft.y` | number |  |
| `result[].fields.servicesYouMayNeedGenericDrugsOutOfNetworkProvider.location.topRight.x` | number |  |
| `result[].fields.servicesYouMayNeedGenericDrugsOutOfNetworkProvider.location.topRight.y` | number |  |
| `result[].fields.servicesYouMayNeedGenericDrugsOutOfNetworkProvider.type` | string |  |
| `result[].fields.servicesYouMayNeedGenericDrugsOutOfNetworkProvider.value` | string |  |
| `result[].fields.servicesYouMayNeedHabilitationServicesInNetworkProvider.confidence` | number |  |
| `result[].fields.servicesYouMayNeedHabilitationServicesInNetworkProvider.key` | string |  |
| `result[].fields.servicesYouMayNeedHabilitationServicesInNetworkProvider.location.bottomLeft.x` | number |  |
| `result[].fields.servicesYouMayNeedHabilitationServicesInNetworkProvider.location.bottomLeft.y` | number |  |
| `result[].fields.servicesYouMayNeedHabilitationServicesInNetworkProvider.location.bottomRight.x` | number |  |
| `result[].fields.servicesYouMayNeedHabilitationServicesInNetworkProvider.location.bottomRight.y` | number |  |
| `result[].fields.servicesYouMayNeedHabilitationServicesInNetworkProvider.location.pageNumber` | number |  |
| `result[].fields.servicesYouMayNeedHabilitationServicesInNetworkProvider.location.topLeft.x` | number |  |
| `result[].fields.servicesYouMayNeedHabilitationServicesInNetworkProvider.location.topLeft.y` | number |  |
| `result[].fields.servicesYouMayNeedHabilitationServicesInNetworkProvider.location.topRight.x` | number |  |
| `result[].fields.servicesYouMayNeedHabilitationServicesInNetworkProvider.location.topRight.y` | number |  |
| `result[].fields.servicesYouMayNeedHabilitationServicesInNetworkProvider.type` | string |  |
| `result[].fields.servicesYouMayNeedHabilitationServicesInNetworkProvider.value` | string |  |
| `result[].fields.servicesYouMayNeedHabilitationServicesOutOfNetworkProvider.confidence` | number |  |
| `result[].fields.servicesYouMayNeedHabilitationServicesOutOfNetworkProvider.key` | string |  |
| `result[].fields.servicesYouMayNeedHabilitationServicesOutOfNetworkProvider.location.bottomLeft.x` | number |  |
| `result[].fields.servicesYouMayNeedHabilitationServicesOutOfNetworkProvider.location.bottomLeft.y` | number |  |
| `result[].fields.servicesYouMayNeedHabilitationServicesOutOfNetworkProvider.location.bottomRight.x` | number |  |
| `result[].fields.servicesYouMayNeedHabilitationServicesOutOfNetworkProvider.location.bottomRight.y` | number |  |
| `result[].fields.servicesYouMayNeedHabilitationServicesOutOfNetworkProvider.location.pageNumber` | number |  |
| `result[].fields.servicesYouMayNeedHabilitationServicesOutOfNetworkProvider.location.topLeft.x` | number |  |
| `result[].fields.servicesYouMayNeedHabilitationServicesOutOfNetworkProvider.location.topLeft.y` | number |  |
| `result[].fields.servicesYouMayNeedHabilitationServicesOutOfNetworkProvider.location.topRight.x` | number |  |
| `result[].fields.servicesYouMayNeedHabilitationServicesOutOfNetworkProvider.location.topRight.y` | number |  |
| `result[].fields.servicesYouMayNeedHabilitationServicesOutOfNetworkProvider.type` | string |  |
| `result[].fields.servicesYouMayNeedHabilitationServicesOutOfNetworkProvider.value` | string |  |
| `result[].fields.servicesYouMayNeedHomeHealthcareInNetworkProvider.confidence` | number |  |
| `result[].fields.servicesYouMayNeedHomeHealthcareInNetworkProvider.key` | string |  |
| `result[].fields.servicesYouMayNeedHomeHealthcareInNetworkProvider.location.bottomLeft.x` | number |  |
| `result[].fields.servicesYouMayNeedHomeHealthcareInNetworkProvider.location.bottomLeft.y` | number |  |
| `result[].fields.servicesYouMayNeedHomeHealthcareInNetworkProvider.location.bottomRight.x` | number |  |
| `result[].fields.servicesYouMayNeedHomeHealthcareInNetworkProvider.location.bottomRight.y` | number |  |
| `result[].fields.servicesYouMayNeedHomeHealthcareInNetworkProvider.location.pageNumber` | number |  |
| `result[].fields.servicesYouMayNeedHomeHealthcareInNetworkProvider.location.topLeft.x` | number |  |
| `result[].fields.servicesYouMayNeedHomeHealthcareInNetworkProvider.location.topLeft.y` | number |  |
| `result[].fields.servicesYouMayNeedHomeHealthcareInNetworkProvider.location.topRight.x` | number |  |
| `result[].fields.servicesYouMayNeedHomeHealthcareInNetworkProvider.location.topRight.y` | number |  |
| `result[].fields.servicesYouMayNeedHomeHealthcareInNetworkProvider.type` | string |  |
| `result[].fields.servicesYouMayNeedHomeHealthcareInNetworkProvider.value` | string |  |
| `result[].fields.servicesYouMayNeedHomeHealthcareOutOfNetworkProvider.confidence` | number |  |
| `result[].fields.servicesYouMayNeedHomeHealthcareOutOfNetworkProvider.key` | string |  |
| `result[].fields.servicesYouMayNeedHomeHealthcareOutOfNetworkProvider.location.bottomLeft.x` | number |  |
| `result[].fields.servicesYouMayNeedHomeHealthcareOutOfNetworkProvider.location.bottomLeft.y` | number |  |
| `result[].fields.servicesYouMayNeedHomeHealthcareOutOfNetworkProvider.location.bottomRight.x` | number |  |
| `result[].fields.servicesYouMayNeedHomeHealthcareOutOfNetworkProvider.location.bottomRight.y` | number |  |
| `result[].fields.servicesYouMayNeedHomeHealthcareOutOfNetworkProvider.location.pageNumber` | number |  |
| `result[].fields.servicesYouMayNeedHomeHealthcareOutOfNetworkProvider.location.topLeft.x` | number |  |
| `result[].fields.servicesYouMayNeedHomeHealthcareOutOfNetworkProvider.location.topLeft.y` | number |  |
| `result[].fields.servicesYouMayNeedHomeHealthcareOutOfNetworkProvider.location.topRight.x` | number |  |
| `result[].fields.servicesYouMayNeedHomeHealthcareOutOfNetworkProvider.location.topRight.y` | number |  |
| `result[].fields.servicesYouMayNeedHomeHealthcareOutOfNetworkProvider.type` | string |  |
| `result[].fields.servicesYouMayNeedHomeHealthcareOutOfNetworkProvider.value` | string |  |
| `result[].fields.servicesYouMayNeedHospiceServicesInNetworkProvider.confidence` | number |  |
| `result[].fields.servicesYouMayNeedHospiceServicesInNetworkProvider.key` | string |  |
| `result[].fields.servicesYouMayNeedHospiceServicesInNetworkProvider.location.bottomLeft.x` | number |  |
| `result[].fields.servicesYouMayNeedHospiceServicesInNetworkProvider.location.bottomLeft.y` | number |  |
| `result[].fields.servicesYouMayNeedHospiceServicesInNetworkProvider.location.bottomRight.x` | number |  |
| `result[].fields.servicesYouMayNeedHospiceServicesInNetworkProvider.location.bottomRight.y` | number |  |
| `result[].fields.servicesYouMayNeedHospiceServicesInNetworkProvider.location.pageNumber` | number |  |
| `result[].fields.servicesYouMayNeedHospiceServicesInNetworkProvider.location.topLeft.x` | number |  |
| `result[].fields.servicesYouMayNeedHospiceServicesInNetworkProvider.location.topLeft.y` | number |  |
| `result[].fields.servicesYouMayNeedHospiceServicesInNetworkProvider.location.topRight.x` | number |  |
| `result[].fields.servicesYouMayNeedHospiceServicesInNetworkProvider.location.topRight.y` | number |  |
| `result[].fields.servicesYouMayNeedHospiceServicesInNetworkProvider.type` | string |  |
| `result[].fields.servicesYouMayNeedHospiceServicesInNetworkProvider.value` | string |  |
| `result[].fields.servicesYouMayNeedHospiceServicesOutOfNetworkProvider.confidence` | number |  |
| `result[].fields.servicesYouMayNeedHospiceServicesOutOfNetworkProvider.key` | string |  |
| `result[].fields.servicesYouMayNeedHospiceServicesOutOfNetworkProvider.location.bottomLeft.x` | number |  |
| `result[].fields.servicesYouMayNeedHospiceServicesOutOfNetworkProvider.location.bottomLeft.y` | number |  |
| `result[].fields.servicesYouMayNeedHospiceServicesOutOfNetworkProvider.location.bottomRight.x` | number |  |
| `result[].fields.servicesYouMayNeedHospiceServicesOutOfNetworkProvider.location.bottomRight.y` | number |  |
| `result[].fields.servicesYouMayNeedHospiceServicesOutOfNetworkProvider.location.pageNumber` | number |  |
| `result[].fields.servicesYouMayNeedHospiceServicesOutOfNetworkProvider.location.topLeft.x` | number |  |
| `result[].fields.servicesYouMayNeedHospiceServicesOutOfNetworkProvider.location.topLeft.y` | number |  |
| `result[].fields.servicesYouMayNeedHospiceServicesOutOfNetworkProvider.location.topRight.x` | number |  |
| `result[].fields.servicesYouMayNeedHospiceServicesOutOfNetworkProvider.location.topRight.y` | number |  |
| `result[].fields.servicesYouMayNeedHospiceServicesOutOfNetworkProvider.type` | string |  |
| `result[].fields.servicesYouMayNeedHospiceServicesOutOfNetworkProvider.value` | string |  |
| `result[].fields.servicesYouMayNeedHospitalStayFacilityFeeInNetworkProvider.confidence` | number |  |
| `result[].fields.servicesYouMayNeedHospitalStayFacilityFeeInNetworkProvider.key` | string |  |
| `result[].fields.servicesYouMayNeedHospitalStayFacilityFeeInNetworkProvider.location.bottomLeft.x` | number |  |
| `result[].fields.servicesYouMayNeedHospitalStayFacilityFeeInNetworkProvider.location.bottomLeft.y` | number |  |
| `result[].fields.servicesYouMayNeedHospitalStayFacilityFeeInNetworkProvider.location.bottomRight.x` | number |  |
| `result[].fields.servicesYouMayNeedHospitalStayFacilityFeeInNetworkProvider.location.bottomRight.y` | number |  |
| `result[].fields.servicesYouMayNeedHospitalStayFacilityFeeInNetworkProvider.location.pageNumber` | number |  |
| `result[].fields.servicesYouMayNeedHospitalStayFacilityFeeInNetworkProvider.location.topLeft.x` | number |  |
| `result[].fields.servicesYouMayNeedHospitalStayFacilityFeeInNetworkProvider.location.topLeft.y` | number |  |
| `result[].fields.servicesYouMayNeedHospitalStayFacilityFeeInNetworkProvider.location.topRight.x` | number |  |
| `result[].fields.servicesYouMayNeedHospitalStayFacilityFeeInNetworkProvider.location.topRight.y` | number |  |
| `result[].fields.servicesYouMayNeedHospitalStayFacilityFeeInNetworkProvider.type` | string |  |
| `result[].fields.servicesYouMayNeedHospitalStayFacilityFeeInNetworkProvider.value` | string |  |
| `result[].fields.servicesYouMayNeedHospitalStayFacilityFeeOutOfNetworkProvider.confidence` | number |  |
| `result[].fields.servicesYouMayNeedHospitalStayFacilityFeeOutOfNetworkProvider.key` | string |  |
| `result[].fields.servicesYouMayNeedHospitalStayFacilityFeeOutOfNetworkProvider.location.bottomLeft.x` | number |  |
| `result[].fields.servicesYouMayNeedHospitalStayFacilityFeeOutOfNetworkProvider.location.bottomLeft.y` | number |  |
| `result[].fields.servicesYouMayNeedHospitalStayFacilityFeeOutOfNetworkProvider.location.bottomRight.x` | number |  |
| `result[].fields.servicesYouMayNeedHospitalStayFacilityFeeOutOfNetworkProvider.location.bottomRight.y` | number |  |
| `result[].fields.servicesYouMayNeedHospitalStayFacilityFeeOutOfNetworkProvider.location.pageNumber` | number |  |
| `result[].fields.servicesYouMayNeedHospitalStayFacilityFeeOutOfNetworkProvider.location.topLeft.x` | number |  |
| `result[].fields.servicesYouMayNeedHospitalStayFacilityFeeOutOfNetworkProvider.location.topLeft.y` | number |  |
| `result[].fields.servicesYouMayNeedHospitalStayFacilityFeeOutOfNetworkProvider.location.topRight.x` | number |  |
| `result[].fields.servicesYouMayNeedHospitalStayFacilityFeeOutOfNetworkProvider.location.topRight.y` | number |  |
| `result[].fields.servicesYouMayNeedHospitalStayFacilityFeeOutOfNetworkProvider.type` | string |  |
| `result[].fields.servicesYouMayNeedHospitalStayFacilityFeeOutOfNetworkProvider.value` | string |  |
| `result[].fields.servicesYouMayNeedHospitalStayPhysicianFeeInNetworkProvider.confidence` | number |  |
| `result[].fields.servicesYouMayNeedHospitalStayPhysicianFeeInNetworkProvider.key` | string |  |
| `result[].fields.servicesYouMayNeedHospitalStayPhysicianFeeInNetworkProvider.location.bottomLeft.x` | number |  |
| `result[].fields.servicesYouMayNeedHospitalStayPhysicianFeeInNetworkProvider.location.bottomLeft.y` | number |  |
| `result[].fields.servicesYouMayNeedHospitalStayPhysicianFeeInNetworkProvider.location.bottomRight.x` | number |  |
| `result[].fields.servicesYouMayNeedHospitalStayPhysicianFeeInNetworkProvider.location.bottomRight.y` | number |  |
| `result[].fields.servicesYouMayNeedHospitalStayPhysicianFeeInNetworkProvider.location.pageNumber` | number |  |
| `result[].fields.servicesYouMayNeedHospitalStayPhysicianFeeInNetworkProvider.location.topLeft.x` | number |  |
| `result[].fields.servicesYouMayNeedHospitalStayPhysicianFeeInNetworkProvider.location.topLeft.y` | number |  |
| `result[].fields.servicesYouMayNeedHospitalStayPhysicianFeeInNetworkProvider.location.topRight.x` | number |  |
| `result[].fields.servicesYouMayNeedHospitalStayPhysicianFeeInNetworkProvider.location.topRight.y` | number |  |
| `result[].fields.servicesYouMayNeedHospitalStayPhysicianFeeInNetworkProvider.type` | string |  |
| `result[].fields.servicesYouMayNeedHospitalStayPhysicianFeeInNetworkProvider.value` | string |  |
| `result[].fields.servicesYouMayNeedHospitalStayPhysicianFeeOutOfNetworkProvider.confidence` | number |  |
| `result[].fields.servicesYouMayNeedHospitalStayPhysicianFeeOutOfNetworkProvider.key` | string |  |
| `result[].fields.servicesYouMayNeedHospitalStayPhysicianFeeOutOfNetworkProvider.location.bottomLeft.x` | number |  |
| `result[].fields.servicesYouMayNeedHospitalStayPhysicianFeeOutOfNetworkProvider.location.bottomLeft.y` | number |  |
| `result[].fields.servicesYouMayNeedHospitalStayPhysicianFeeOutOfNetworkProvider.location.bottomRight.x` | number |  |
| `result[].fields.servicesYouMayNeedHospitalStayPhysicianFeeOutOfNetworkProvider.location.bottomRight.y` | number |  |
| `result[].fields.servicesYouMayNeedHospitalStayPhysicianFeeOutOfNetworkProvider.location.pageNumber` | number |  |
| `result[].fields.servicesYouMayNeedHospitalStayPhysicianFeeOutOfNetworkProvider.location.topLeft.x` | number |  |
| `result[].fields.servicesYouMayNeedHospitalStayPhysicianFeeOutOfNetworkProvider.location.topLeft.y` | number |  |
| `result[].fields.servicesYouMayNeedHospitalStayPhysicianFeeOutOfNetworkProvider.location.topRight.x` | number |  |
| `result[].fields.servicesYouMayNeedHospitalStayPhysicianFeeOutOfNetworkProvider.location.topRight.y` | number |  |
| `result[].fields.servicesYouMayNeedHospitalStayPhysicianFeeOutOfNetworkProvider.type` | string |  |
| `result[].fields.servicesYouMayNeedHospitalStayPhysicianFeeOutOfNetworkProvider.value` | string |  |
| `result[].fields.servicesYouMayNeedImagingInNetworkProvider.confidence` | number |  |
| `result[].fields.servicesYouMayNeedImagingInNetworkProvider.key` | string |  |
| `result[].fields.servicesYouMayNeedImagingInNetworkProvider.location.bottomLeft.x` | number |  |
| `result[].fields.servicesYouMayNeedImagingInNetworkProvider.location.bottomLeft.y` | number |  |
| `result[].fields.servicesYouMayNeedImagingInNetworkProvider.location.bottomRight.x` | number |  |
| `result[].fields.servicesYouMayNeedImagingInNetworkProvider.location.bottomRight.y` | number |  |
| `result[].fields.servicesYouMayNeedImagingInNetworkProvider.location.pageNumber` | number |  |
| `result[].fields.servicesYouMayNeedImagingInNetworkProvider.location.topLeft.x` | number |  |
| `result[].fields.servicesYouMayNeedImagingInNetworkProvider.location.topLeft.y` | number |  |
| `result[].fields.servicesYouMayNeedImagingInNetworkProvider.location.topRight.x` | number |  |
| `result[].fields.servicesYouMayNeedImagingInNetworkProvider.location.topRight.y` | number |  |
| `result[].fields.servicesYouMayNeedImagingInNetworkProvider.type` | string |  |
| `result[].fields.servicesYouMayNeedImagingInNetworkProvider.value` | string |  |
| `result[].fields.servicesYouMayNeedImagingOutOfNetworkProvider.confidence` | number |  |
| `result[].fields.servicesYouMayNeedImagingOutOfNetworkProvider.key` | string |  |
| `result[].fields.servicesYouMayNeedImagingOutOfNetworkProvider.location.bottomLeft.x` | number |  |
| `result[].fields.servicesYouMayNeedImagingOutOfNetworkProvider.location.bottomLeft.y` | number |  |
| `result[].fields.servicesYouMayNeedImagingOutOfNetworkProvider.location.bottomRight.x` | number |  |
| `result[].fields.servicesYouMayNeedImagingOutOfNetworkProvider.location.bottomRight.y` | number |  |
| `result[].fields.servicesYouMayNeedImagingOutOfNetworkProvider.location.pageNumber` | number |  |
| `result[].fields.servicesYouMayNeedImagingOutOfNetworkProvider.location.topLeft.x` | number |  |
| `result[].fields.servicesYouMayNeedImagingOutOfNetworkProvider.location.topLeft.y` | number |  |
| `result[].fields.servicesYouMayNeedImagingOutOfNetworkProvider.location.topRight.x` | number |  |
| `result[].fields.servicesYouMayNeedImagingOutOfNetworkProvider.location.topRight.y` | number |  |
| `result[].fields.servicesYouMayNeedImagingOutOfNetworkProvider.type` | string |  |
| `result[].fields.servicesYouMayNeedImagingOutOfNetworkProvider.value` | string |  |
| `result[].fields.servicesYouMayNeedInpatientMentalServicesInNetworkProvider.confidence` | number |  |
| `result[].fields.servicesYouMayNeedInpatientMentalServicesInNetworkProvider.key` | string |  |
| `result[].fields.servicesYouMayNeedInpatientMentalServicesInNetworkProvider.location.bottomLeft.x` | number |  |
| `result[].fields.servicesYouMayNeedInpatientMentalServicesInNetworkProvider.location.bottomLeft.y` | number |  |
| `result[].fields.servicesYouMayNeedInpatientMentalServicesInNetworkProvider.location.bottomRight.x` | number |  |
| `result[].fields.servicesYouMayNeedInpatientMentalServicesInNetworkProvider.location.bottomRight.y` | number |  |
| `result[].fields.servicesYouMayNeedInpatientMentalServicesInNetworkProvider.location.pageNumber` | number |  |
| `result[].fields.servicesYouMayNeedInpatientMentalServicesInNetworkProvider.location.topLeft.x` | number |  |
| `result[].fields.servicesYouMayNeedInpatientMentalServicesInNetworkProvider.location.topLeft.y` | number |  |
| `result[].fields.servicesYouMayNeedInpatientMentalServicesInNetworkProvider.location.topRight.x` | number |  |
| `result[].fields.servicesYouMayNeedInpatientMentalServicesInNetworkProvider.location.topRight.y` | number |  |
| `result[].fields.servicesYouMayNeedInpatientMentalServicesInNetworkProvider.type` | string |  |
| `result[].fields.servicesYouMayNeedInpatientMentalServicesInNetworkProvider.value` | string |  |
| `result[].fields.servicesYouMayNeedInpatientMentalServicesOutOfNetworkProvider.confidence` | number |  |
| `result[].fields.servicesYouMayNeedInpatientMentalServicesOutOfNetworkProvider.key` | string |  |
| `result[].fields.servicesYouMayNeedInpatientMentalServicesOutOfNetworkProvider.location.bottomLeft.x` | number |  |
| `result[].fields.servicesYouMayNeedInpatientMentalServicesOutOfNetworkProvider.location.bottomLeft.y` | number |  |
| `result[].fields.servicesYouMayNeedInpatientMentalServicesOutOfNetworkProvider.location.bottomRight.x` | number |  |
| `result[].fields.servicesYouMayNeedInpatientMentalServicesOutOfNetworkProvider.location.bottomRight.y` | number |  |
| `result[].fields.servicesYouMayNeedInpatientMentalServicesOutOfNetworkProvider.location.pageNumber` | number |  |
| `result[].fields.servicesYouMayNeedInpatientMentalServicesOutOfNetworkProvider.location.topLeft.x` | number |  |
| `result[].fields.servicesYouMayNeedInpatientMentalServicesOutOfNetworkProvider.location.topLeft.y` | number |  |
| `result[].fields.servicesYouMayNeedInpatientMentalServicesOutOfNetworkProvider.location.topRight.x` | number |  |
| `result[].fields.servicesYouMayNeedInpatientMentalServicesOutOfNetworkProvider.location.topRight.y` | number |  |
| `result[].fields.servicesYouMayNeedInpatientMentalServicesOutOfNetworkProvider.type` | string |  |
| `result[].fields.servicesYouMayNeedInpatientMentalServicesOutOfNetworkProvider.value` | string |  |
| `result[].fields.servicesYouMayNeedMailOrderDrugCoefficient.confidence` | number |  |
| `result[].fields.servicesYouMayNeedMailOrderDrugCoefficient.key` | string |  |
| `result[].fields.servicesYouMayNeedMailOrderDrugCoefficient.type` | string |  |
| `result[].fields.servicesYouMayNeedMailOrderDrugCoefficient.value` | number |  |
| `result[].fields.servicesYouMayNeedNonPreferredBrandDrugsInNetworkProvider.confidence` | number |  |
| `result[].fields.servicesYouMayNeedNonPreferredBrandDrugsInNetworkProvider.key` | string |  |
| `result[].fields.servicesYouMayNeedNonPreferredBrandDrugsInNetworkProvider.location.bottomLeft.x` | number |  |
| `result[].fields.servicesYouMayNeedNonPreferredBrandDrugsInNetworkProvider.location.bottomLeft.y` | number |  |
| `result[].fields.servicesYouMayNeedNonPreferredBrandDrugsInNetworkProvider.location.bottomRight.x` | number |  |
| `result[].fields.servicesYouMayNeedNonPreferredBrandDrugsInNetworkProvider.location.bottomRight.y` | number |  |
| `result[].fields.servicesYouMayNeedNonPreferredBrandDrugsInNetworkProvider.location.pageNumber` | number |  |
| `result[].fields.servicesYouMayNeedNonPreferredBrandDrugsInNetworkProvider.location.topLeft.x` | number |  |
| `result[].fields.servicesYouMayNeedNonPreferredBrandDrugsInNetworkProvider.location.topLeft.y` | number |  |
| `result[].fields.servicesYouMayNeedNonPreferredBrandDrugsInNetworkProvider.location.topRight.x` | number |  |
| `result[].fields.servicesYouMayNeedNonPreferredBrandDrugsInNetworkProvider.location.topRight.y` | number |  |
| `result[].fields.servicesYouMayNeedNonPreferredBrandDrugsInNetworkProvider.type` | string |  |
| `result[].fields.servicesYouMayNeedNonPreferredBrandDrugsInNetworkProvider.value` | string |  |
| `result[].fields.servicesYouMayNeedNonPreferredBrandDrugsOutOfNetworkProvider.confidence` | number |  |
| `result[].fields.servicesYouMayNeedNonPreferredBrandDrugsOutOfNetworkProvider.key` | string |  |
| `result[].fields.servicesYouMayNeedNonPreferredBrandDrugsOutOfNetworkProvider.location.bottomLeft.x` | number |  |
| `result[].fields.servicesYouMayNeedNonPreferredBrandDrugsOutOfNetworkProvider.location.bottomLeft.y` | number |  |
| `result[].fields.servicesYouMayNeedNonPreferredBrandDrugsOutOfNetworkProvider.location.bottomRight.x` | number |  |
| `result[].fields.servicesYouMayNeedNonPreferredBrandDrugsOutOfNetworkProvider.location.bottomRight.y` | number |  |
| `result[].fields.servicesYouMayNeedNonPreferredBrandDrugsOutOfNetworkProvider.location.pageNumber` | number |  |
| `result[].fields.servicesYouMayNeedNonPreferredBrandDrugsOutOfNetworkProvider.location.topLeft.x` | number |  |
| `result[].fields.servicesYouMayNeedNonPreferredBrandDrugsOutOfNetworkProvider.location.topLeft.y` | number |  |
| `result[].fields.servicesYouMayNeedNonPreferredBrandDrugsOutOfNetworkProvider.location.topRight.x` | number |  |
| `result[].fields.servicesYouMayNeedNonPreferredBrandDrugsOutOfNetworkProvider.location.topRight.y` | number |  |
| `result[].fields.servicesYouMayNeedNonPreferredBrandDrugsOutOfNetworkProvider.type` | string |  |
| `result[].fields.servicesYouMayNeedNonPreferredBrandDrugsOutOfNetworkProvider.value` | string |  |
| `result[].fields.servicesYouMayNeedOutOfNetworkCoverage.confidence` | number |  |
| `result[].fields.servicesYouMayNeedOutOfNetworkCoverage.key` | string |  |
| `result[].fields.servicesYouMayNeedOutOfNetworkCoverage.type` | string |  |
| `result[].fields.servicesYouMayNeedOutOfNetworkCoverage.value` | string |  |
| `result[].fields.servicesYouMayNeedOutpatientFacilityFeeInNetworkProvider.confidence` | number |  |
| `result[].fields.servicesYouMayNeedOutpatientFacilityFeeInNetworkProvider.key` | string |  |
| `result[].fields.servicesYouMayNeedOutpatientFacilityFeeInNetworkProvider.location.bottomLeft.x` | number |  |
| `result[].fields.servicesYouMayNeedOutpatientFacilityFeeInNetworkProvider.location.bottomLeft.y` | number |  |
| `result[].fields.servicesYouMayNeedOutpatientFacilityFeeInNetworkProvider.location.bottomRight.x` | number |  |
| `result[].fields.servicesYouMayNeedOutpatientFacilityFeeInNetworkProvider.location.bottomRight.y` | number |  |
| `result[].fields.servicesYouMayNeedOutpatientFacilityFeeInNetworkProvider.location.pageNumber` | number |  |
| `result[].fields.servicesYouMayNeedOutpatientFacilityFeeInNetworkProvider.location.topLeft.x` | number |  |
| `result[].fields.servicesYouMayNeedOutpatientFacilityFeeInNetworkProvider.location.topLeft.y` | number |  |
| `result[].fields.servicesYouMayNeedOutpatientFacilityFeeInNetworkProvider.location.topRight.x` | number |  |
| `result[].fields.servicesYouMayNeedOutpatientFacilityFeeInNetworkProvider.location.topRight.y` | number |  |
| `result[].fields.servicesYouMayNeedOutpatientFacilityFeeInNetworkProvider.type` | string |  |
| `result[].fields.servicesYouMayNeedOutpatientFacilityFeeInNetworkProvider.value` | string |  |
| `result[].fields.servicesYouMayNeedOutpatientFacilityFeeOutOfNetworkProvider.confidence` | number |  |
| `result[].fields.servicesYouMayNeedOutpatientFacilityFeeOutOfNetworkProvider.key` | string |  |
| `result[].fields.servicesYouMayNeedOutpatientFacilityFeeOutOfNetworkProvider.location.bottomLeft.x` | number |  |
| `result[].fields.servicesYouMayNeedOutpatientFacilityFeeOutOfNetworkProvider.location.bottomLeft.y` | number |  |
| `result[].fields.servicesYouMayNeedOutpatientFacilityFeeOutOfNetworkProvider.location.bottomRight.x` | number |  |
| `result[].fields.servicesYouMayNeedOutpatientFacilityFeeOutOfNetworkProvider.location.bottomRight.y` | number |  |
| `result[].fields.servicesYouMayNeedOutpatientFacilityFeeOutOfNetworkProvider.location.pageNumber` | number |  |
| `result[].fields.servicesYouMayNeedOutpatientFacilityFeeOutOfNetworkProvider.location.topLeft.x` | number |  |
| `result[].fields.servicesYouMayNeedOutpatientFacilityFeeOutOfNetworkProvider.location.topLeft.y` | number |  |
| `result[].fields.servicesYouMayNeedOutpatientFacilityFeeOutOfNetworkProvider.location.topRight.x` | number |  |
| `result[].fields.servicesYouMayNeedOutpatientFacilityFeeOutOfNetworkProvider.location.topRight.y` | number |  |
| `result[].fields.servicesYouMayNeedOutpatientFacilityFeeOutOfNetworkProvider.type` | string |  |
| `result[].fields.servicesYouMayNeedOutpatientFacilityFeeOutOfNetworkProvider.value` | string |  |
| `result[].fields.servicesYouMayNeedOutpatientMentalServicesInNetworkProvider.confidence` | number |  |
| `result[].fields.servicesYouMayNeedOutpatientMentalServicesInNetworkProvider.key` | string |  |
| `result[].fields.servicesYouMayNeedOutpatientMentalServicesInNetworkProvider.location.bottomLeft.x` | number |  |
| `result[].fields.servicesYouMayNeedOutpatientMentalServicesInNetworkProvider.location.bottomLeft.y` | number |  |
| `result[].fields.servicesYouMayNeedOutpatientMentalServicesInNetworkProvider.location.bottomRight.x` | number |  |
| `result[].fields.servicesYouMayNeedOutpatientMentalServicesInNetworkProvider.location.bottomRight.y` | number |  |
| `result[].fields.servicesYouMayNeedOutpatientMentalServicesInNetworkProvider.location.pageNumber` | number |  |
| `result[].fields.servicesYouMayNeedOutpatientMentalServicesInNetworkProvider.location.topLeft.x` | number |  |
| `result[].fields.servicesYouMayNeedOutpatientMentalServicesInNetworkProvider.location.topLeft.y` | number |  |
| `result[].fields.servicesYouMayNeedOutpatientMentalServicesInNetworkProvider.location.topRight.x` | number |  |
| `result[].fields.servicesYouMayNeedOutpatientMentalServicesInNetworkProvider.location.topRight.y` | number |  |
| `result[].fields.servicesYouMayNeedOutpatientMentalServicesInNetworkProvider.type` | string |  |
| `result[].fields.servicesYouMayNeedOutpatientMentalServicesInNetworkProvider.value` | string |  |
| `result[].fields.servicesYouMayNeedOutpatientMentalServicesOutOfNetworkProvider.confidence` | number |  |
| `result[].fields.servicesYouMayNeedOutpatientMentalServicesOutOfNetworkProvider.key` | string |  |
| `result[].fields.servicesYouMayNeedOutpatientMentalServicesOutOfNetworkProvider.location.bottomLeft.x` | number |  |
| `result[].fields.servicesYouMayNeedOutpatientMentalServicesOutOfNetworkProvider.location.bottomLeft.y` | number |  |
| `result[].fields.servicesYouMayNeedOutpatientMentalServicesOutOfNetworkProvider.location.bottomRight.x` | number |  |
| `result[].fields.servicesYouMayNeedOutpatientMentalServicesOutOfNetworkProvider.location.bottomRight.y` | number |  |
| `result[].fields.servicesYouMayNeedOutpatientMentalServicesOutOfNetworkProvider.location.pageNumber` | number |  |
| `result[].fields.servicesYouMayNeedOutpatientMentalServicesOutOfNetworkProvider.location.topLeft.x` | number |  |
| `result[].fields.servicesYouMayNeedOutpatientMentalServicesOutOfNetworkProvider.location.topLeft.y` | number |  |
| `result[].fields.servicesYouMayNeedOutpatientMentalServicesOutOfNetworkProvider.location.topRight.x` | number |  |
| `result[].fields.servicesYouMayNeedOutpatientMentalServicesOutOfNetworkProvider.location.topRight.y` | number |  |
| `result[].fields.servicesYouMayNeedOutpatientMentalServicesOutOfNetworkProvider.type` | string |  |
| `result[].fields.servicesYouMayNeedOutpatientMentalServicesOutOfNetworkProvider.value` | string |  |
| `result[].fields.servicesYouMayNeedOutpatientPhysicianFeeInNetworkProvider.confidence` | number |  |
| `result[].fields.servicesYouMayNeedOutpatientPhysicianFeeInNetworkProvider.key` | string |  |
| `result[].fields.servicesYouMayNeedOutpatientPhysicianFeeInNetworkProvider.location.bottomLeft.x` | number |  |
| `result[].fields.servicesYouMayNeedOutpatientPhysicianFeeInNetworkProvider.location.bottomLeft.y` | number |  |
| `result[].fields.servicesYouMayNeedOutpatientPhysicianFeeInNetworkProvider.location.bottomRight.x` | number |  |
| `result[].fields.servicesYouMayNeedOutpatientPhysicianFeeInNetworkProvider.location.bottomRight.y` | number |  |
| `result[].fields.servicesYouMayNeedOutpatientPhysicianFeeInNetworkProvider.location.pageNumber` | number |  |
| `result[].fields.servicesYouMayNeedOutpatientPhysicianFeeInNetworkProvider.location.topLeft.x` | number |  |
| `result[].fields.servicesYouMayNeedOutpatientPhysicianFeeInNetworkProvider.location.topLeft.y` | number |  |
| `result[].fields.servicesYouMayNeedOutpatientPhysicianFeeInNetworkProvider.location.topRight.x` | number |  |
| `result[].fields.servicesYouMayNeedOutpatientPhysicianFeeInNetworkProvider.location.topRight.y` | number |  |
| `result[].fields.servicesYouMayNeedOutpatientPhysicianFeeInNetworkProvider.type` | string |  |
| `result[].fields.servicesYouMayNeedOutpatientPhysicianFeeInNetworkProvider.value` | string |  |
| `result[].fields.servicesYouMayNeedOutpatientPhysicianFeeOutOfNetworkProvider.confidence` | number |  |
| `result[].fields.servicesYouMayNeedOutpatientPhysicianFeeOutOfNetworkProvider.key` | string |  |
| `result[].fields.servicesYouMayNeedOutpatientPhysicianFeeOutOfNetworkProvider.location.bottomLeft.x` | number |  |
| `result[].fields.servicesYouMayNeedOutpatientPhysicianFeeOutOfNetworkProvider.location.bottomLeft.y` | number |  |
| `result[].fields.servicesYouMayNeedOutpatientPhysicianFeeOutOfNetworkProvider.location.bottomRight.x` | number |  |
| `result[].fields.servicesYouMayNeedOutpatientPhysicianFeeOutOfNetworkProvider.location.bottomRight.y` | number |  |
| `result[].fields.servicesYouMayNeedOutpatientPhysicianFeeOutOfNetworkProvider.location.pageNumber` | number |  |
| `result[].fields.servicesYouMayNeedOutpatientPhysicianFeeOutOfNetworkProvider.location.topLeft.x` | number |  |
| `result[].fields.servicesYouMayNeedOutpatientPhysicianFeeOutOfNetworkProvider.location.topLeft.y` | number |  |
| `result[].fields.servicesYouMayNeedOutpatientPhysicianFeeOutOfNetworkProvider.location.topRight.x` | number |  |
| `result[].fields.servicesYouMayNeedOutpatientPhysicianFeeOutOfNetworkProvider.location.topRight.y` | number |  |
| `result[].fields.servicesYouMayNeedOutpatientPhysicianFeeOutOfNetworkProvider.type` | string |  |
| `result[].fields.servicesYouMayNeedOutpatientPhysicianFeeOutOfNetworkProvider.value` | string |  |
| `result[].fields.servicesYouMayNeedPreferredBrandDrugsInNetworkProvider.confidence` | number |  |
| `result[].fields.servicesYouMayNeedPreferredBrandDrugsInNetworkProvider.key` | string |  |
| `result[].fields.servicesYouMayNeedPreferredBrandDrugsInNetworkProvider.location.bottomLeft.x` | number |  |
| `result[].fields.servicesYouMayNeedPreferredBrandDrugsInNetworkProvider.location.bottomLeft.y` | number |  |
| `result[].fields.servicesYouMayNeedPreferredBrandDrugsInNetworkProvider.location.bottomRight.x` | number |  |
| `result[].fields.servicesYouMayNeedPreferredBrandDrugsInNetworkProvider.location.bottomRight.y` | number |  |
| `result[].fields.servicesYouMayNeedPreferredBrandDrugsInNetworkProvider.location.pageNumber` | number |  |
| `result[].fields.servicesYouMayNeedPreferredBrandDrugsInNetworkProvider.location.topLeft.x` | number |  |
| `result[].fields.servicesYouMayNeedPreferredBrandDrugsInNetworkProvider.location.topLeft.y` | number |  |
| `result[].fields.servicesYouMayNeedPreferredBrandDrugsInNetworkProvider.location.topRight.x` | number |  |
| `result[].fields.servicesYouMayNeedPreferredBrandDrugsInNetworkProvider.location.topRight.y` | number |  |
| `result[].fields.servicesYouMayNeedPreferredBrandDrugsInNetworkProvider.type` | string |  |
| `result[].fields.servicesYouMayNeedPreferredBrandDrugsInNetworkProvider.value` | string |  |
| `result[].fields.servicesYouMayNeedPreferredBrandDrugsOutOfNetworkProvider.confidence` | number |  |
| `result[].fields.servicesYouMayNeedPreferredBrandDrugsOutOfNetworkProvider.key` | string |  |
| `result[].fields.servicesYouMayNeedPreferredBrandDrugsOutOfNetworkProvider.location.bottomLeft.x` | number |  |
| `result[].fields.servicesYouMayNeedPreferredBrandDrugsOutOfNetworkProvider.location.bottomLeft.y` | number |  |
| `result[].fields.servicesYouMayNeedPreferredBrandDrugsOutOfNetworkProvider.location.bottomRight.x` | number |  |
| `result[].fields.servicesYouMayNeedPreferredBrandDrugsOutOfNetworkProvider.location.bottomRight.y` | number |  |
| `result[].fields.servicesYouMayNeedPreferredBrandDrugsOutOfNetworkProvider.location.pageNumber` | number |  |
| `result[].fields.servicesYouMayNeedPreferredBrandDrugsOutOfNetworkProvider.location.topLeft.x` | number |  |
| `result[].fields.servicesYouMayNeedPreferredBrandDrugsOutOfNetworkProvider.location.topLeft.y` | number |  |
| `result[].fields.servicesYouMayNeedPreferredBrandDrugsOutOfNetworkProvider.location.topRight.x` | number |  |
| `result[].fields.servicesYouMayNeedPreferredBrandDrugsOutOfNetworkProvider.location.topRight.y` | number |  |
| `result[].fields.servicesYouMayNeedPreferredBrandDrugsOutOfNetworkProvider.type` | string |  |
| `result[].fields.servicesYouMayNeedPreferredBrandDrugsOutOfNetworkProvider.value` | string |  |
| `result[].fields.servicesYouMayNeedPreventiveCareInNetworkProvider.confidence` | number |  |
| `result[].fields.servicesYouMayNeedPreventiveCareInNetworkProvider.key` | string |  |
| `result[].fields.servicesYouMayNeedPreventiveCareInNetworkProvider.location.bottomLeft.x` | number |  |
| `result[].fields.servicesYouMayNeedPreventiveCareInNetworkProvider.location.bottomLeft.y` | number |  |
| `result[].fields.servicesYouMayNeedPreventiveCareInNetworkProvider.location.bottomRight.x` | number |  |
| `result[].fields.servicesYouMayNeedPreventiveCareInNetworkProvider.location.bottomRight.y` | number |  |
| `result[].fields.servicesYouMayNeedPreventiveCareInNetworkProvider.location.pageNumber` | number |  |
| `result[].fields.servicesYouMayNeedPreventiveCareInNetworkProvider.location.topLeft.x` | number |  |
| `result[].fields.servicesYouMayNeedPreventiveCareInNetworkProvider.location.topLeft.y` | number |  |
| `result[].fields.servicesYouMayNeedPreventiveCareInNetworkProvider.location.topRight.x` | number |  |
| `result[].fields.servicesYouMayNeedPreventiveCareInNetworkProvider.location.topRight.y` | number |  |
| `result[].fields.servicesYouMayNeedPreventiveCareInNetworkProvider.type` | string |  |
| `result[].fields.servicesYouMayNeedPreventiveCareInNetworkProvider.value` | string |  |
| `result[].fields.servicesYouMayNeedPreventiveCareOutOfNetworkProvider.confidence` | number |  |
| `result[].fields.servicesYouMayNeedPreventiveCareOutOfNetworkProvider.key` | string |  |
| `result[].fields.servicesYouMayNeedPreventiveCareOutOfNetworkProvider.location.bottomLeft.x` | number |  |
| `result[].fields.servicesYouMayNeedPreventiveCareOutOfNetworkProvider.location.bottomLeft.y` | number |  |
| `result[].fields.servicesYouMayNeedPreventiveCareOutOfNetworkProvider.location.bottomRight.x` | number |  |
| `result[].fields.servicesYouMayNeedPreventiveCareOutOfNetworkProvider.location.bottomRight.y` | number |  |
| `result[].fields.servicesYouMayNeedPreventiveCareOutOfNetworkProvider.location.pageNumber` | number |  |
| `result[].fields.servicesYouMayNeedPreventiveCareOutOfNetworkProvider.location.topLeft.x` | number |  |
| `result[].fields.servicesYouMayNeedPreventiveCareOutOfNetworkProvider.location.topLeft.y` | number |  |
| `result[].fields.servicesYouMayNeedPreventiveCareOutOfNetworkProvider.location.topRight.x` | number |  |
| `result[].fields.servicesYouMayNeedPreventiveCareOutOfNetworkProvider.location.topRight.y` | number |  |
| `result[].fields.servicesYouMayNeedPreventiveCareOutOfNetworkProvider.type` | string |  |
| `result[].fields.servicesYouMayNeedPreventiveCareOutOfNetworkProvider.value` | string |  |
| `result[].fields.servicesYouMayNeedPrimaryCareInNetworkProvider.confidence` | number |  |
| `result[].fields.servicesYouMayNeedPrimaryCareInNetworkProvider.key` | string |  |
| `result[].fields.servicesYouMayNeedPrimaryCareInNetworkProvider.location.bottomLeft.x` | number |  |
| `result[].fields.servicesYouMayNeedPrimaryCareInNetworkProvider.location.bottomLeft.y` | number |  |
| `result[].fields.servicesYouMayNeedPrimaryCareInNetworkProvider.location.bottomRight.x` | number |  |
| `result[].fields.servicesYouMayNeedPrimaryCareInNetworkProvider.location.bottomRight.y` | number |  |
| `result[].fields.servicesYouMayNeedPrimaryCareInNetworkProvider.location.pageNumber` | number |  |
| `result[].fields.servicesYouMayNeedPrimaryCareInNetworkProvider.location.topLeft.x` | number |  |
| `result[].fields.servicesYouMayNeedPrimaryCareInNetworkProvider.location.topLeft.y` | number |  |
| `result[].fields.servicesYouMayNeedPrimaryCareInNetworkProvider.location.topRight.x` | number |  |
| `result[].fields.servicesYouMayNeedPrimaryCareInNetworkProvider.location.topRight.y` | number |  |
| `result[].fields.servicesYouMayNeedPrimaryCareInNetworkProvider.type` | string |  |
| `result[].fields.servicesYouMayNeedPrimaryCareInNetworkProvider.value` | string |  |
| `result[].fields.servicesYouMayNeedPrimaryCareOutOfNetworkProvider.confidence` | number |  |
| `result[].fields.servicesYouMayNeedPrimaryCareOutOfNetworkProvider.key` | string |  |
| `result[].fields.servicesYouMayNeedPrimaryCareOutOfNetworkProvider.location.bottomLeft.x` | number |  |
| `result[].fields.servicesYouMayNeedPrimaryCareOutOfNetworkProvider.location.bottomLeft.y` | number |  |
| `result[].fields.servicesYouMayNeedPrimaryCareOutOfNetworkProvider.location.bottomRight.x` | number |  |
| `result[].fields.servicesYouMayNeedPrimaryCareOutOfNetworkProvider.location.bottomRight.y` | number |  |
| `result[].fields.servicesYouMayNeedPrimaryCareOutOfNetworkProvider.location.pageNumber` | number |  |
| `result[].fields.servicesYouMayNeedPrimaryCareOutOfNetworkProvider.location.topLeft.x` | number |  |
| `result[].fields.servicesYouMayNeedPrimaryCareOutOfNetworkProvider.location.topLeft.y` | number |  |
| `result[].fields.servicesYouMayNeedPrimaryCareOutOfNetworkProvider.location.topRight.x` | number |  |
| `result[].fields.servicesYouMayNeedPrimaryCareOutOfNetworkProvider.location.topRight.y` | number |  |
| `result[].fields.servicesYouMayNeedPrimaryCareOutOfNetworkProvider.type` | string |  |
| `result[].fields.servicesYouMayNeedPrimaryCareOutOfNetworkProvider.value` | string |  |
| `result[].fields.servicesYouMayNeedRehabilitationServicesInNetworkProvider.confidence` | number |  |
| `result[].fields.servicesYouMayNeedRehabilitationServicesInNetworkProvider.key` | string |  |
| `result[].fields.servicesYouMayNeedRehabilitationServicesInNetworkProvider.location.bottomLeft.x` | number |  |
| `result[].fields.servicesYouMayNeedRehabilitationServicesInNetworkProvider.location.bottomLeft.y` | number |  |
| `result[].fields.servicesYouMayNeedRehabilitationServicesInNetworkProvider.location.bottomRight.x` | number |  |
| `result[].fields.servicesYouMayNeedRehabilitationServicesInNetworkProvider.location.bottomRight.y` | number |  |
| `result[].fields.servicesYouMayNeedRehabilitationServicesInNetworkProvider.location.pageNumber` | number |  |
| `result[].fields.servicesYouMayNeedRehabilitationServicesInNetworkProvider.location.topLeft.x` | number |  |
| `result[].fields.servicesYouMayNeedRehabilitationServicesInNetworkProvider.location.topLeft.y` | number |  |
| `result[].fields.servicesYouMayNeedRehabilitationServicesInNetworkProvider.location.topRight.x` | number |  |
| `result[].fields.servicesYouMayNeedRehabilitationServicesInNetworkProvider.location.topRight.y` | number |  |
| `result[].fields.servicesYouMayNeedRehabilitationServicesInNetworkProvider.type` | string |  |
| `result[].fields.servicesYouMayNeedRehabilitationServicesInNetworkProvider.value` | string |  |
| `result[].fields.servicesYouMayNeedRehabilitationServicesOutOfNetworkProvider.confidence` | number |  |
| `result[].fields.servicesYouMayNeedRehabilitationServicesOutOfNetworkProvider.key` | string |  |
| `result[].fields.servicesYouMayNeedRehabilitationServicesOutOfNetworkProvider.location.bottomLeft.x` | number |  |
| `result[].fields.servicesYouMayNeedRehabilitationServicesOutOfNetworkProvider.location.bottomLeft.y` | number |  |
| `result[].fields.servicesYouMayNeedRehabilitationServicesOutOfNetworkProvider.location.bottomRight.x` | number |  |
| `result[].fields.servicesYouMayNeedRehabilitationServicesOutOfNetworkProvider.location.bottomRight.y` | number |  |
| `result[].fields.servicesYouMayNeedRehabilitationServicesOutOfNetworkProvider.location.pageNumber` | number |  |
| `result[].fields.servicesYouMayNeedRehabilitationServicesOutOfNetworkProvider.location.topLeft.x` | number |  |
| `result[].fields.servicesYouMayNeedRehabilitationServicesOutOfNetworkProvider.location.topLeft.y` | number |  |
| `result[].fields.servicesYouMayNeedRehabilitationServicesOutOfNetworkProvider.location.topRight.x` | number |  |
| `result[].fields.servicesYouMayNeedRehabilitationServicesOutOfNetworkProvider.location.topRight.y` | number |  |
| `result[].fields.servicesYouMayNeedRehabilitationServicesOutOfNetworkProvider.type` | string |  |
| `result[].fields.servicesYouMayNeedRehabilitationServicesOutOfNetworkProvider.value` | string |  |
| `result[].fields.servicesYouMayNeedSkilledNursingCareInNetworkProvider.confidence` | number |  |
| `result[].fields.servicesYouMayNeedSkilledNursingCareInNetworkProvider.key` | string |  |
| `result[].fields.servicesYouMayNeedSkilledNursingCareInNetworkProvider.location.bottomLeft.x` | number |  |
| `result[].fields.servicesYouMayNeedSkilledNursingCareInNetworkProvider.location.bottomLeft.y` | number |  |
| `result[].fields.servicesYouMayNeedSkilledNursingCareInNetworkProvider.location.bottomRight.x` | number |  |
| `result[].fields.servicesYouMayNeedSkilledNursingCareInNetworkProvider.location.bottomRight.y` | number |  |
| `result[].fields.servicesYouMayNeedSkilledNursingCareInNetworkProvider.location.pageNumber` | number |  |
| `result[].fields.servicesYouMayNeedSkilledNursingCareInNetworkProvider.location.topLeft.x` | number |  |
| `result[].fields.servicesYouMayNeedSkilledNursingCareInNetworkProvider.location.topLeft.y` | number |  |
| `result[].fields.servicesYouMayNeedSkilledNursingCareInNetworkProvider.location.topRight.x` | number |  |
| `result[].fields.servicesYouMayNeedSkilledNursingCareInNetworkProvider.location.topRight.y` | number |  |
| `result[].fields.servicesYouMayNeedSkilledNursingCareInNetworkProvider.type` | string |  |
| `result[].fields.servicesYouMayNeedSkilledNursingCareInNetworkProvider.value` | string |  |
| `result[].fields.servicesYouMayNeedSkilledNursingCareOutOfNetworkProvider.confidence` | number |  |
| `result[].fields.servicesYouMayNeedSkilledNursingCareOutOfNetworkProvider.key` | string |  |
| `result[].fields.servicesYouMayNeedSkilledNursingCareOutOfNetworkProvider.location.bottomLeft.x` | number |  |
| `result[].fields.servicesYouMayNeedSkilledNursingCareOutOfNetworkProvider.location.bottomLeft.y` | number |  |
| `result[].fields.servicesYouMayNeedSkilledNursingCareOutOfNetworkProvider.location.bottomRight.x` | number |  |
| `result[].fields.servicesYouMayNeedSkilledNursingCareOutOfNetworkProvider.location.bottomRight.y` | number |  |
| `result[].fields.servicesYouMayNeedSkilledNursingCareOutOfNetworkProvider.location.pageNumber` | number |  |
| `result[].fields.servicesYouMayNeedSkilledNursingCareOutOfNetworkProvider.location.topLeft.x` | number |  |
| `result[].fields.servicesYouMayNeedSkilledNursingCareOutOfNetworkProvider.location.topLeft.y` | number |  |
| `result[].fields.servicesYouMayNeedSkilledNursingCareOutOfNetworkProvider.location.topRight.x` | number |  |
| `result[].fields.servicesYouMayNeedSkilledNursingCareOutOfNetworkProvider.location.topRight.y` | number |  |
| `result[].fields.servicesYouMayNeedSkilledNursingCareOutOfNetworkProvider.type` | string |  |
| `result[].fields.servicesYouMayNeedSkilledNursingCareOutOfNetworkProvider.value` | string |  |
| `result[].fields.servicesYouMayNeedSpecialistVisitInNetworkProvider.confidence` | number |  |
| `result[].fields.servicesYouMayNeedSpecialistVisitInNetworkProvider.key` | string |  |
| `result[].fields.servicesYouMayNeedSpecialistVisitInNetworkProvider.location.bottomLeft.x` | number |  |
| `result[].fields.servicesYouMayNeedSpecialistVisitInNetworkProvider.location.bottomLeft.y` | number |  |
| `result[].fields.servicesYouMayNeedSpecialistVisitInNetworkProvider.location.bottomRight.x` | number |  |
| `result[].fields.servicesYouMayNeedSpecialistVisitInNetworkProvider.location.bottomRight.y` | number |  |
| `result[].fields.servicesYouMayNeedSpecialistVisitInNetworkProvider.location.pageNumber` | number |  |
| `result[].fields.servicesYouMayNeedSpecialistVisitInNetworkProvider.location.topLeft.x` | number |  |
| `result[].fields.servicesYouMayNeedSpecialistVisitInNetworkProvider.location.topLeft.y` | number |  |
| `result[].fields.servicesYouMayNeedSpecialistVisitInNetworkProvider.location.topRight.x` | number |  |
| `result[].fields.servicesYouMayNeedSpecialistVisitInNetworkProvider.location.topRight.y` | number |  |
| `result[].fields.servicesYouMayNeedSpecialistVisitInNetworkProvider.type` | string |  |
| `result[].fields.servicesYouMayNeedSpecialistVisitInNetworkProvider.value` | string |  |
| `result[].fields.servicesYouMayNeedSpecialistVisitOutOfNetworkProvider.confidence` | number |  |
| `result[].fields.servicesYouMayNeedSpecialistVisitOutOfNetworkProvider.key` | string |  |
| `result[].fields.servicesYouMayNeedSpecialistVisitOutOfNetworkProvider.location.bottomLeft.x` | number |  |
| `result[].fields.servicesYouMayNeedSpecialistVisitOutOfNetworkProvider.location.bottomLeft.y` | number |  |
| `result[].fields.servicesYouMayNeedSpecialistVisitOutOfNetworkProvider.location.bottomRight.x` | number |  |
| `result[].fields.servicesYouMayNeedSpecialistVisitOutOfNetworkProvider.location.bottomRight.y` | number |  |
| `result[].fields.servicesYouMayNeedSpecialistVisitOutOfNetworkProvider.location.pageNumber` | number |  |
| `result[].fields.servicesYouMayNeedSpecialistVisitOutOfNetworkProvider.location.topLeft.x` | number |  |
| `result[].fields.servicesYouMayNeedSpecialistVisitOutOfNetworkProvider.location.topLeft.y` | number |  |
| `result[].fields.servicesYouMayNeedSpecialistVisitOutOfNetworkProvider.location.topRight.x` | number |  |
| `result[].fields.servicesYouMayNeedSpecialistVisitOutOfNetworkProvider.location.topRight.y` | number |  |
| `result[].fields.servicesYouMayNeedSpecialistVisitOutOfNetworkProvider.type` | string |  |
| `result[].fields.servicesYouMayNeedSpecialistVisitOutOfNetworkProvider.value` | string |  |
| `result[].fields.servicesYouMayNeedSpecialtyDrugsInNetworkProvider.confidence` | number |  |
| `result[].fields.servicesYouMayNeedSpecialtyDrugsInNetworkProvider.key` | string |  |
| `result[].fields.servicesYouMayNeedSpecialtyDrugsInNetworkProvider.location.bottomLeft.x` | number |  |
| `result[].fields.servicesYouMayNeedSpecialtyDrugsInNetworkProvider.location.bottomLeft.y` | number |  |
| `result[].fields.servicesYouMayNeedSpecialtyDrugsInNetworkProvider.location.bottomRight.x` | number |  |
| `result[].fields.servicesYouMayNeedSpecialtyDrugsInNetworkProvider.location.bottomRight.y` | number |  |
| `result[].fields.servicesYouMayNeedSpecialtyDrugsInNetworkProvider.location.pageNumber` | number |  |
| `result[].fields.servicesYouMayNeedSpecialtyDrugsInNetworkProvider.location.topLeft.x` | number |  |
| `result[].fields.servicesYouMayNeedSpecialtyDrugsInNetworkProvider.location.topLeft.y` | number |  |
| `result[].fields.servicesYouMayNeedSpecialtyDrugsInNetworkProvider.location.topRight.x` | number |  |
| `result[].fields.servicesYouMayNeedSpecialtyDrugsInNetworkProvider.location.topRight.y` | number |  |
| `result[].fields.servicesYouMayNeedSpecialtyDrugsInNetworkProvider.type` | string |  |
| `result[].fields.servicesYouMayNeedSpecialtyDrugsInNetworkProvider.value` | string |  |
| `result[].fields.servicesYouMayNeedSpecialtyDrugsOutOfNetworkProvider.confidence` | number |  |
| `result[].fields.servicesYouMayNeedSpecialtyDrugsOutOfNetworkProvider.key` | string |  |
| `result[].fields.servicesYouMayNeedSpecialtyDrugsOutOfNetworkProvider.location.bottomLeft.x` | number |  |
| `result[].fields.servicesYouMayNeedSpecialtyDrugsOutOfNetworkProvider.location.bottomLeft.y` | number |  |
| `result[].fields.servicesYouMayNeedSpecialtyDrugsOutOfNetworkProvider.location.bottomRight.x` | number |  |
| `result[].fields.servicesYouMayNeedSpecialtyDrugsOutOfNetworkProvider.location.bottomRight.y` | number |  |
| `result[].fields.servicesYouMayNeedSpecialtyDrugsOutOfNetworkProvider.location.pageNumber` | number |  |
| `result[].fields.servicesYouMayNeedSpecialtyDrugsOutOfNetworkProvider.location.topLeft.x` | number |  |
| `result[].fields.servicesYouMayNeedSpecialtyDrugsOutOfNetworkProvider.location.topLeft.y` | number |  |
| `result[].fields.servicesYouMayNeedSpecialtyDrugsOutOfNetworkProvider.location.topRight.x` | number |  |
| `result[].fields.servicesYouMayNeedSpecialtyDrugsOutOfNetworkProvider.location.topRight.y` | number |  |
| `result[].fields.servicesYouMayNeedSpecialtyDrugsOutOfNetworkProvider.type` | string |  |
| `result[].fields.servicesYouMayNeedSpecialtyDrugsOutOfNetworkProvider.value` | string |  |
| `result[].fields.servicesYouMayNeedUrgentCareInNetworkProvider.confidence` | number |  |
| `result[].fields.servicesYouMayNeedUrgentCareInNetworkProvider.key` | string |  |
| `result[].fields.servicesYouMayNeedUrgentCareInNetworkProvider.location.bottomLeft.x` | number |  |
| `result[].fields.servicesYouMayNeedUrgentCareInNetworkProvider.location.bottomLeft.y` | number |  |
| `result[].fields.servicesYouMayNeedUrgentCareInNetworkProvider.location.bottomRight.x` | number |  |
| `result[].fields.servicesYouMayNeedUrgentCareInNetworkProvider.location.bottomRight.y` | number |  |
| `result[].fields.servicesYouMayNeedUrgentCareInNetworkProvider.location.pageNumber` | number |  |
| `result[].fields.servicesYouMayNeedUrgentCareInNetworkProvider.location.topLeft.x` | number |  |
| `result[].fields.servicesYouMayNeedUrgentCareInNetworkProvider.location.topLeft.y` | number |  |
| `result[].fields.servicesYouMayNeedUrgentCareInNetworkProvider.location.topRight.x` | number |  |
| `result[].fields.servicesYouMayNeedUrgentCareInNetworkProvider.location.topRight.y` | number |  |
| `result[].fields.servicesYouMayNeedUrgentCareInNetworkProvider.type` | string |  |
| `result[].fields.servicesYouMayNeedUrgentCareInNetworkProvider.value` | string |  |
| `result[].fields.servicesYouMayNeedUrgentCareOutOfNetworkProvider.confidence` | number |  |
| `result[].fields.servicesYouMayNeedUrgentCareOutOfNetworkProvider.key` | string |  |
| `result[].fields.servicesYouMayNeedUrgentCareOutOfNetworkProvider.location.bottomLeft.x` | number |  |
| `result[].fields.servicesYouMayNeedUrgentCareOutOfNetworkProvider.location.bottomLeft.y` | number |  |
| `result[].fields.servicesYouMayNeedUrgentCareOutOfNetworkProvider.location.bottomRight.x` | number |  |
| `result[].fields.servicesYouMayNeedUrgentCareOutOfNetworkProvider.location.bottomRight.y` | number |  |
| `result[].fields.servicesYouMayNeedUrgentCareOutOfNetworkProvider.location.pageNumber` | number |  |
| `result[].fields.servicesYouMayNeedUrgentCareOutOfNetworkProvider.location.topLeft.x` | number |  |
| `result[].fields.servicesYouMayNeedUrgentCareOutOfNetworkProvider.location.topLeft.y` | number |  |
| `result[].fields.servicesYouMayNeedUrgentCareOutOfNetworkProvider.location.topRight.x` | number |  |
| `result[].fields.servicesYouMayNeedUrgentCareOutOfNetworkProvider.location.topRight.y` | number |  |
| `result[].fields.servicesYouMayNeedUrgentCareOutOfNetworkProvider.type` | string |  |
| `result[].fields.servicesYouMayNeedUrgentCareOutOfNetworkProvider.value` | string |  |
| `result[].model.confidence` | number |  |
| `result[].model.isValid` | boolean |  |
| `result[].model.name` | string |  |
| `result[].model.shape` | string |  |
| `result[].model.type` | string |  |
| `result[].ocr` | string |  |
| `result[].status` | string |  |
| `result[].uuid` | string |  |
| `reviewedBy[]` | object |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Base64.ai API, this operation is `GET /api/result/:resultUuid` (base URL `https://base64.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-result.md) for the provider-specific parameters and requirements.

