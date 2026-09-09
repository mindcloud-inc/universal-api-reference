# Walmart: Get Spec

Retrieve specifications for a specified Product Type or a set of Product Types.

```
GET https://connect.mindcloud.co/v1/universal/walmart/latest/actions/get-spec
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Walmart `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/walmart/latest/actions/get-spec?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/walmart/latest/actions/get-spec?${params}`, {
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
| `feedType` | string | no | The type of feed, which specifies the nature of the update. Example: `MP_WFS_ITEM` |
| `version` | string | no | Enter the item specification version. Example: `5.0.20250121-19_24_23-api` |
| `productTypes` | string | no | An item type with a specific set of attributes that define the product. Example: `Shirts`, `Shoes`, `Baby Blankets` Accepts multiple values as an array. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "$schema": "string",
      "additionalProperties": true,
      "properties": {
        "mPItem": {
          "$schema": "string",
          "items": {
            "$schema": "string",
            "additionalProperties": true,
            "properties": {
              "orderable": {
                "$schema": "string",
                "additionalProperties": true,
                "allOf": [
                  {
                    "if": {
                      "anyOf": [
                        {
                          "properties": {
                            "chemicalAerosolPesticide": {
                              "enum": [
                                "string"
                              ],
                              "type": "string"
                            }
                          },
                          "required": [
                            "string"
                          ]
                        }
                      ]
                    },
                    "then": {
                      "required": [
                        "string"
                      ]
                    }
                  }
                ],
                "properties": {
                  "batterySize": {
                    "comments": "string",
                    "description": "string",
                    "enum": [
                      "string"
                    ],
                    "examples": "string",
                    "title": "string",
                    "type": "string"
                  },
                  "batteryTechnologyType": {
                    "comments": "string",
                    "description": "string",
                    "enum": [
                      "string"
                    ],
                    "examples": "string",
                    "title": "string",
                    "type": "string"
                  },
                  "chemicalAerosolPesticide": {
                    "comments": "string",
                    "description": "string",
                    "enum": [
                      "string"
                    ],
                    "examples": "string",
                    "title": "string",
                    "type": "string"
                  },
                  "electronicsIndicator": {
                    "comments": "string",
                    "description": "string",
                    "enum": [
                      "string"
                    ],
                    "examples": "string",
                    "title": "string",
                    "type": "string"
                  },
                  "endDate": {
                    "comments": "string",
                    "description": "string",
                    "examples": [
                      "string"
                    ],
                    "format": "string",
                    "title": "string",
                    "type": "string"
                  },
                  "externalProductIdentifier": {
                    "$schema": "string",
                    "comments": "string",
                    "description": "string",
                    "examples": "string",
                    "items": {
                      "$schema": "string",
                      "additionalProperties": true,
                      "properties": {
                        "externalProductId": {
                          "comments": "string",
                          "description": "string",
                          "examples": [
                            "string"
                          ],
                          "maxLength": 1,
                          "minLength": 1,
                          "title": "string",
                          "type": "string"
                        },
                        "externalProductIdType": {
                          "comments": "string",
                          "description": "string",
                          "enum": [
                            "string"
                          ],
                          "examples": "string",
                          "title": "string",
                          "type": "string"
                        }
                      },
                      "required": [
                        "string"
                      ],
                      "type": "string"
                    },
                    "minItems": 1,
                    "title": "string",
                    "type": "string"
                  },
                  "hasBatteries": {
                    "comments": "string",
                    "description": "string",
                    "enum": [
                      "string"
                    ],
                    "examples": "string",
                    "title": "string",
                    "type": "string"
                  },
                  "labelImage": {
                    "$schema": "string",
                    "comments": "string",
                    "description": "string",
                    "examples": "string",
                    "items": {
                      "$schema": "string",
                      "additionalProperties": true,
                      "properties": {
                        "labelImageContains": {
                          "comments": "string",
                          "description": "string",
                          "enum": [
                            "string"
                          ],
                          "examples": "string",
                          "title": "string",
                          "type": "string"
                        },
                        "labelImageURL": {
                          "comments": "https://example.com",
                          "description": "https://example.com",
                          "examples": [
                            "https://example.com"
                          ],
                          "format": "https://example.com",
                          "maxLength": 1,
                          "minLength": 1,
                          "title": "https://example.com",
                          "type": "https://example.com"
                        }
                      },
                      "type": "string"
                    },
                    "minItems": 1,
                    "title": "string",
                    "type": "string"
                  },
                  "lithiumIonBatteries": {
                    "$schema": "string",
                    "additionalProperties": true,
                    "comments": "string",
                    "description": "string",
                    "examples": "string",
                    "properties": {
                      "batteryWattHour": {
                        "comments": "string",
                        "description": "string",
                        "examples": "string",
                        "maximum": 1,
                        "minimum": 1,
                        "multipleOf": 1,
                        "title": "string",
                        "type": "string"
                      },
                      "ionBatteryFormFactor": {
                        "comments": "string",
                        "description": "string",
                        "enum": [
                          "string"
                        ],
                        "examples": "string",
                        "title": "string",
                        "type": "string"
                      },
                      "ionBatteryModel": {
                        "comments": "string",
                        "description": "string",
                        "examples": [
                          "string"
                        ],
                        "maxLength": 1,
                        "minLength": 1,
                        "title": "string",
                        "type": "string"
                      },
                      "ionBatteryWeight": {
                        "comments": "string",
                        "description": "string",
                        "examples": [
                          "string"
                        ],
                        "maximum": 1,
                        "minimum": 1,
                        "multipleOf": 1,
                        "title": "string",
                        "type": "string"
                      },
                      "ionIncludedBatteryPackaging": {
                        "comments": "string",
                        "description": "string",
                        "enum": [
                          "string"
                        ],
                        "examples": "string",
                        "title": "string",
                        "type": "string"
                      },
                      "ionNumberOfBatteries": {
                        "comments": "string",
                        "description": "string",
                        "examples": [
                          "string"
                        ],
                        "maximum": 1,
                        "minimum": 1,
                        "title": "string",
                        "type": "string"
                      },
                      "ionNumberOfBatteryCells": {
                        "comments": "string",
                        "description": "string",
                        "examples": [
                          "string"
                        ],
                        "maximum": 1,
                        "minimum": 1,
                        "title": "string",
                        "type": "string"
                      }
                    },
                    "required": [
                      "string"
                    ],
                    "title": "string",
                    "type": "string"
                  },
                  "lithiumMetalBatteries": {
                    "$schema": "string",
                    "additionalProperties": true,
                    "comments": "string",
                    "description": "string",
                    "examples": "string",
                    "properties": {
                      "lithiumMetalContentWeight": {
                        "comments": "string",
                        "description": "string",
                        "examples": "string",
                        "maximum": 1,
                        "minimum": 1,
                        "multipleOf": 1,
                        "title": "string",
                        "type": "string"
                      },
                      "metalBatteryCellCount": {
                        "comments": "string",
                        "description": "string",
                        "examples": [
                          "string"
                        ],
                        "maximum": 1,
                        "minimum": 1,
                        "title": "string",
                        "type": "string"
                      },
                      "metalBatteryFormFactor": {
                        "comments": "string",
                        "description": "string",
                        "enum": [
                          "string"
                        ],
                        "examples": "string",
                        "title": "string",
                        "type": "string"
                      },
                      "metalBatteryModel": {
                        "comments": "string",
                        "description": "string",
                        "examples": [
                          "string"
                        ],
                        "maxLength": 1,
                        "minLength": 1,
                        "title": "string",
                        "type": "string"
                      },
                      "metalBatteryWeight": {
                        "comments": "string",
                        "description": "string",
                        "examples": [
                          "string"
                        ],
                        "maximum": 1,
                        "minimum": 1,
                        "multipleOf": 1,
                        "title": "string",
                        "type": "string"
                      },
                      "metalIncludedBatteryPackaging": {
                        "comments": "string",
                        "description": "string",
                        "enum": [
                          "string"
                        ],
                        "examples": "string",
                        "title": "string",
                        "type": "string"
                      },
                      "metalNumberOfBatteries": {
                        "comments": "string",
                        "description": "string",
                        "examples": [
                          "string"
                        ],
                        "maximum": 1,
                        "minimum": 1,
                        "title": "string",
                        "type": "string"
                      }
                    },
                    "required": [
                      "string"
                    ],
                    "title": "string",
                    "type": "string"
                  },
                  "mustShipAlone": {
                    "comments": "string",
                    "description": "string",
                    "enum": [
                      "string"
                    ],
                    "examples": "string",
                    "title": "string",
                    "type": "string"
                  },
                  "numberOfHazardousComponents": {
                    "comments": "string",
                    "description": "string",
                    "examples": [
                      "string"
                    ],
                    "maximum": 1,
                    "minimum": 1,
                    "title": "string",
                    "type": "string"
                  },
                  "price": {
                    "comments": "string",
                    "description": "string",
                    "examples": [
                      "string"
                    ],
                    "maximum": 1,
                    "minimum": 1,
                    "multipleOf": 1,
                    "title": "string",
                    "type": "string"
                  },
                  "productIdentifiers": {
                    "$schema": "string",
                    "additionalProperties": true,
                    "comments": "string",
                    "description": "string",
                    "examples": "string",
                    "properties": {
                      "productId": {
                        "comments": "string",
                        "description": "string",
                        "examples": [
                          "string"
                        ],
                        "maxLength": 1,
                        "minLength": 1,
                        "title": "string",
                        "type": "string"
                      },
                      "productIdType": {
                        "comments": "string",
                        "description": "string",
                        "enum": [
                          "string"
                        ],
                        "examples": "string",
                        "title": "string",
                        "type": "string"
                      }
                    },
                    "required": [
                      "string"
                    ],
                    "title": "string",
                    "type": "string"
                  },
                  "requiredStorageCondition": {
                    "$schema": "string",
                    "comments": "string",
                    "description": "string",
                    "examples": "string",
                    "items": {
                      "enum": [
                        "string"
                      ],
                      "type": "string"
                    },
                    "minItems": 1,
                    "title": "string",
                    "type": "string"
                  },
                  "safetyDataSheet": {
                    "$schema": "string",
                    "comments": "string",
                    "description": "string",
                    "examples": "string",
                    "items": {
                      "format": "string",
                      "maxLength": 1,
                      "type": "string"
                    },
                    "minItems": 1,
                    "title": "string",
                    "type": "string"
                  },
                  "shipsInOriginalPackaging": {
                    "comments": "string",
                    "description": "string",
                    "enum": [
                      "string"
                    ],
                    "examples": "string",
                    "title": "string",
                    "type": "string"
                  },
                  "sku": {
                    "comments": "string",
                    "description": "string",
                    "examples": [
                      "string"
                    ],
                    "maxLength": 1,
                    "minLength": 1,
                    "title": "string",
                    "type": "string"
                  },
                  "skuUpdate": {
                    "comments": "string",
                    "description": "string",
                    "enum": [
                      "string"
                    ],
                    "examples": "string",
                    "title": "string",
                    "type": "string"
                  },
                  "startDate": {
                    "comments": "string",
                    "description": "string",
                    "examples": [
                      "string"
                    ],
                    "format": "string",
                    "title": "string",
                    "type": "string"
                  },
                  "stateRestrictions": {
                    "$schema": "string",
                    "comments": "string",
                    "description": "string",
                    "examples": "string",
                    "items": {
                      "$schema": "string",
                      "additionalProperties": true,
                      "properties": {
                        "stateRestrictionsText": {
                          "comments": "string",
                          "description": "string",
                          "enum": [
                            "string"
                          ],
                          "examples": "string",
                          "title": "string",
                          "type": "string"
                        },
                        "states": {
                          "comments": "string",
                          "description": "string",
                          "enum": [
                            "string"
                          ],
                          "examples": "string",
                          "title": "string",
                          "type": "string"
                        },
                        "zipCodes": {
                          "comments": "string",
                          "description": "string",
                          "examples": [
                            "string"
                          ],
                          "maxLength": 1,
                          "minLength": 1,
                          "title": "string",
                          "type": "string"
                        }
                      },
                      "required": [
                        "string"
                      ],
                      "type": "string"
                    },
                    "minItems": 1,
                    "title": "string",
                    "type": "string"
                  },
                  "thirdPartyProductFulfillmentType": {
                    "$schema": "string",
                    "comments": "string",
                    "description": "string",
                    "examples": "string",
                    "items": {
                      "enum": [
                        "string"
                      ],
                      "type": "string"
                    },
                    "minItems": 1,
                    "title": "string",
                    "type": "string"
                  }
                },
                "required": [
                  "string"
                ],
                "type": "string"
              },
              "tradeItem": {
                "$schema": "string",
                "additionalProperties": true,
                "properties": {
                  "case": {
                    "$schema": "string",
                    "additionalProperties": true,
                    "comments": "string",
                    "description": "string",
                    "examples": "string",
                    "properties": {
                      "caseDepth": {
                        "comments": "string",
                        "description": "string",
                        "examples": [
                          "string"
                        ],
                        "maximum": 1,
                        "minimum": 1,
                        "multipleOf": 1,
                        "title": "string",
                        "type": "string"
                      },
                      "caseGTIN": {
                        "comments": "string",
                        "description": "string",
                        "examples": [
                          "string"
                        ],
                        "maxLength": 1,
                        "minLength": 1,
                        "title": "string",
                        "type": "string"
                      },
                      "caseHeight": {
                        "comments": "string",
                        "description": "string",
                        "examples": [
                          "string"
                        ],
                        "maximum": 1,
                        "minimum": 1,
                        "multipleOf": 1,
                        "title": "string",
                        "type": "string"
                      },
                      "caseWeight": {
                        "comments": "string",
                        "description": "string",
                        "examples": [
                          "string"
                        ],
                        "maximum": 1,
                        "minimum": 1,
                        "multipleOf": 1,
                        "title": "string",
                        "type": "string"
                      },
                      "caseWidth": {
                        "comments": "string",
                        "description": "string",
                        "examples": [
                          "string"
                        ],
                        "maximum": 1,
                        "minimum": 1,
                        "multipleOf": 1,
                        "title": "string",
                        "type": "string"
                      },
                      "qtySellableItemsCase": {
                        "comments": "string",
                        "description": "string",
                        "examples": [
                          "string"
                        ],
                        "maximum": 1,
                        "minimum": 1,
                        "title": "string",
                        "type": "string"
                      }
                    },
                    "required": [
                      "string"
                    ],
                    "title": "string",
                    "type": "string"
                  },
                  "countryOfOriginAssembly": {
                    "$schema": "string",
                    "comments": "string",
                    "description": "string",
                    "examples": "string",
                    "items": {
                      "enum": [
                        "string"
                      ],
                      "type": "string"
                    },
                    "minItems": 1,
                    "title": "string",
                    "type": "string"
                  },
                  "each": {
                    "$schema": "string",
                    "additionalProperties": true,
                    "comments": "string",
                    "description": "string",
                    "examples": "string",
                    "properties": {
                      "eachDepth": {
                        "comments": "string",
                        "description": "string",
                        "examples": [
                          "string"
                        ],
                        "maximum": 1,
                        "minimum": 1,
                        "multipleOf": 1,
                        "title": "string",
                        "type": "string"
                      },
                      "eachGTIN": {
                        "comments": "string",
                        "description": "string",
                        "examples": [
                          "string"
                        ],
                        "maxLength": 1,
                        "minLength": 1,
                        "title": "string",
                        "type": "string"
                      },
                      "eachHeight": {
                        "comments": "string",
                        "description": "string",
                        "examples": [
                          "string"
                        ],
                        "maximum": 1,
                        "minimum": 1,
                        "multipleOf": 1,
                        "title": "string",
                        "type": "string"
                      },
                      "eachWeight": {
                        "comments": "string",
                        "description": "string",
                        "examples": [
                          "string"
                        ],
                        "maximum": 1,
                        "minimum": 1,
                        "multipleOf": 1,
                        "title": "string",
                        "type": "string"
                      },
                      "eachWidth": {
                        "comments": "string",
                        "description": "string",
                        "examples": [
                          "string"
                        ],
                        "maximum": 1,
                        "minimum": 1,
                        "multipleOf": 1,
                        "title": "string",
                        "type": "string"
                      }
                    },
                    "required": [
                      "string"
                    ],
                    "title": "string",
                    "type": "string"
                  },
                  "innerPack": {
                    "$schema": "string",
                    "additionalProperties": true,
                    "comments": "string",
                    "description": "string",
                    "examples": "string",
                    "properties": {
                      "innerPackDepth": {
                        "comments": "string",
                        "description": "string",
                        "examples": [
                          "string"
                        ],
                        "maximum": 1,
                        "minimum": 1,
                        "multipleOf": 1,
                        "title": "string",
                        "type": "string"
                      },
                      "innerPackGTIN": {
                        "comments": "string",
                        "description": "string",
                        "examples": [
                          "string"
                        ],
                        "maxLength": 1,
                        "minLength": 1,
                        "title": "string",
                        "type": "string"
                      },
                      "innerPackHeight": {
                        "comments": "string",
                        "description": "string",
                        "examples": [
                          "string"
                        ],
                        "maximum": 1,
                        "minimum": 1,
                        "multipleOf": 1,
                        "title": "string",
                        "type": "string"
                      },
                      "innerPackWeight": {
                        "comments": "string",
                        "description": "string",
                        "examples": [
                          "string"
                        ],
                        "maximum": 1,
                        "minimum": 1,
                        "multipleOf": 1,
                        "title": "string",
                        "type": "string"
                      },
                      "innerPackWidth": {
                        "comments": "string",
                        "description": "string",
                        "examples": [
                          "string"
                        ],
                        "maximum": 1,
                        "minimum": 1,
                        "multipleOf": 1,
                        "title": "string",
                        "type": "string"
                      },
                      "qtySellableItemsInnerPack": {
                        "comments": "string",
                        "description": "string",
                        "examples": [
                          "string"
                        ],
                        "maximum": 1,
                        "minimum": 1,
                        "title": "string",
                        "type": "string"
                      }
                    },
                    "required": [
                      "string"
                    ],
                    "title": "string",
                    "type": "string"
                  },
                  "orderableGTIN": {
                    "comments": "string",
                    "description": "string",
                    "examples": [
                      "string"
                    ],
                    "maxLength": 1,
                    "minLength": 1,
                    "title": "string",
                    "type": "string"
                  },
                  "pallet": {
                    "$schema": "string",
                    "additionalProperties": true,
                    "comments": "string",
                    "description": "string",
                    "examples": "string",
                    "properties": {
                      "palletDepth": {
                        "comments": "string",
                        "description": "string",
                        "examples": [
                          "string"
                        ],
                        "maximum": 1,
                        "minimum": 1,
                        "multipleOf": 1,
                        "title": "string",
                        "type": "string"
                      },
                      "palletGTIN": {
                        "comments": "string",
                        "description": "string",
                        "examples": [
                          "string"
                        ],
                        "maxLength": 1,
                        "minLength": 1,
                        "title": "string",
                        "type": "string"
                      },
                      "palletHeight": {
                        "comments": "string",
                        "description": "string",
                        "examples": [
                          "string"
                        ],
                        "maximum": 1,
                        "minimum": 1,
                        "multipleOf": 1,
                        "title": "string",
                        "type": "string"
                      },
                      "palletWeight": {
                        "comments": "string",
                        "description": "string",
                        "examples": [
                          "string"
                        ],
                        "maximum": 1,
                        "minimum": 1,
                        "multipleOf": 1,
                        "title": "string",
                        "type": "string"
                      },
                      "palletWidth": {
                        "comments": "string",
                        "description": "string",
                        "examples": [
                          "string"
                        ],
                        "maximum": 1,
                        "minimum": 1,
                        "multipleOf": 1,
                        "title": "string",
                        "type": "string"
                      },
                      "qtySellableItemsPallet": {
                        "comments": "string",
                        "description": "string",
                        "examples": [
                          "string"
                        ],
                        "maximum": 1,
                        "minimum": 1,
                        "title": "string",
                        "type": "string"
                      }
                    },
                    "required": [
                      "string"
                    ],
                    "title": "string",
                    "type": "string"
                  },
                  "sku": {
                    "comments": "string",
                    "description": "string",
                    "examples": [
                      "string"
                    ],
                    "maxLength": 1,
                    "minLength": 1,
                    "title": "string",
                    "type": "string"
                  }
                },
                "required": [
                  "string"
                ],
                "type": "string"
              },
              "visible": {
                "$schema": "string",
                "additionalProperties": true,
                "oneOf": [
                  {
                    "$schema": "string",
                    "required": [
                      "string"
                    ],
                    "type": "string"
                  }
                ],
                "properties": {
                  "babyBlankets": {
                    "$schema": "string",
                    "additionalProperties": true,
                    "allOf": [
                      {
                        "if": {
                          "properties": {
                            "hasWrittenWarranty": {
                              "enum": [
                                "string"
                              ],
                              "type": "string"
                            }
                          },
                          "required": [
                            "string"
                          ]
                        },
                        "then": {
                          "required": [
                            "string"
                          ]
                        }
                      }
                    ],
                    "properties": {
                      "assembledProductHeight": {
                        "$schema": "string",
                        "additionalProperties": true,
                        "comments": "string",
                        "description": "string",
                        "examples": [
                          "string"
                        ],
                        "properties": {
                          "measure": {
                            "comments": "string",
                            "description": "string",
                            "examples": [
                              "string"
                            ],
                            "maximum": 1,
                            "minimum": 1,
                            "multipleOf": 1,
                            "title": "string",
                            "type": "string"
                          },
                          "unit": {
                            "comments": "string",
                            "description": "string",
                            "enum": [
                              "string"
                            ],
                            "examples": [
                              "string"
                            ],
                            "title": "string",
                            "type": "string"
                          }
                        },
                        "required": [
                          "string"
                        ],
                        "title": "string",
                        "type": "string"
                      },
                      "assembledProductLength": {
                        "$schema": "string",
                        "additionalProperties": true,
                        "comments": "string",
                        "description": "string",
                        "examples": [
                          "string"
                        ],
                        "properties": {
                          "measure": {
                            "comments": "string",
                            "description": "string",
                            "examples": [
                              "string"
                            ],
                            "maximum": 1,
                            "minimum": 1,
                            "multipleOf": 1,
                            "title": "string",
                            "type": "string"
                          },
                          "unit": {
                            "comments": "string",
                            "description": "string",
                            "enum": [
                              "string"
                            ],
                            "examples": [
                              "string"
                            ],
                            "title": "string",
                            "type": "string"
                          }
                        },
                        "required": [
                          "string"
                        ],
                        "title": "string",
                        "type": "string"
                      },
                      "assembledProductWeight": {
                        "$schema": "string",
                        "additionalProperties": true,
                        "comments": "string",
                        "description": "string",
                        "examples": [
                          "string"
                        ],
                        "properties": {
                          "measure": {
                            "comments": "string",
                            "description": "string",
                            "examples": [
                              "string"
                            ],
                            "maximum": 1,
                            "minimum": 1,
                            "multipleOf": 1,
                            "title": "string",
                            "type": "string"
                          },
                          "unit": {
                            "comments": "string",
                            "description": "string",
                            "enum": [
                              "string"
                            ],
                            "examples": [
                              "string"
                            ],
                            "title": "string",
                            "type": "string"
                          }
                        },
                        "required": [
                          "string"
                        ],
                        "title": "string",
                        "type": "string"
                      },
                      "assembledProductWidth": {
                        "$schema": "string",
                        "additionalProperties": true,
                        "comments": "string",
                        "description": "string",
                        "examples": [
                          "string"
                        ],
                        "properties": {
                          "measure": {
                            "comments": "string",
                            "description": "string",
                            "examples": [
                              "string"
                            ],
                            "maximum": 1,
                            "minimum": 1,
                            "multipleOf": 1,
                            "title": "string",
                            "type": "string"
                          },
                          "unit": {
                            "comments": "string",
                            "description": "string",
                            "enum": [
                              "string"
                            ],
                            "examples": [
                              "string"
                            ],
                            "title": "string",
                            "type": "string"
                          }
                        },
                        "required": [
                          "string"
                        ],
                        "title": "string",
                        "type": "string"
                      },
                      "brand": {
                        "comments": "string",
                        "description": "string",
                        "examples": [
                          "string"
                        ],
                        "maxLength": 1,
                        "minLength": 1,
                        "title": "string",
                        "type": "string"
                      },
                      "character": {
                        "$schema": "string",
                        "comments": "string",
                        "description": "string",
                        "examples": [
                          "string"
                        ],
                        "items": {
                          "maxLength": 1,
                          "minLength": 1,
                          "type": "string"
                        },
                        "minItems": 1,
                        "title": "string",
                        "type": "string"
                      },
                      "characterGroup": {
                        "$schema": "string",
                        "comments": "string",
                        "description": "string",
                        "examples": [
                          "string"
                        ],
                        "items": {
                          "maxLength": 1,
                          "minLength": 1,
                          "type": "string"
                        },
                        "minItems": 1,
                        "title": "string",
                        "type": "string"
                      },
                      "collection": {
                        "comments": "string",
                        "description": "string",
                        "examples": [
                          "string"
                        ],
                        "maxLength": 1,
                        "minLength": 1,
                        "title": "string",
                        "type": "string"
                      },
                      "color": {
                        "comments": "string",
                        "description": "string",
                        "examples": [
                          "string"
                        ],
                        "maxLength": 1,
                        "minLength": 1,
                        "title": "string",
                        "type": "string"
                      },
                      "colorCategory": {
                        "$schema": "string",
                        "comments": "string",
                        "description": "string",
                        "examples": "string",
                        "items": {
                          "enum": [
                            "string"
                          ],
                          "type": "string"
                        },
                        "minItems": 1,
                        "title": "string",
                        "type": "string"
                      },
                      "condition": {
                        "comments": "string",
                        "description": "string",
                        "enum": [
                          "string"
                        ],
                        "examples": "string",
                        "title": "string",
                        "type": "string"
                      },
                      "count": {
                        "comments": "string",
                        "description": "string",
                        "examples": [
                          "string"
                        ],
                        "maximum": 1,
                        "minimum": 1,
                        "title": "string",
                        "type": "string"
                      },
                      "countPerPack": {
                        "comments": "string",
                        "description": "string",
                        "examples": [
                          "string"
                        ],
                        "maximum": 1,
                        "minimum": 1,
                        "title": "string",
                        "type": "string"
                      },
                      "fabricCareInstructions": {
                        "$schema": "string",
                        "comments": "string",
                        "description": "string",
                        "examples": [
                          "string"
                        ],
                        "items": {
                          "maxLength": 1,
                          "minLength": 1,
                          "type": "string"
                        },
                        "minItems": 1,
                        "title": "string",
                        "type": "string"
                      },
                      "fabricContent": {
                        "$schema": "string",
                        "comments": "string",
                        "description": "string",
                        "examples": [
                          "string"
                        ],
                        "items": {
                          "$schema": "string",
                          "additionalProperties": true,
                          "properties": {
                            "materialName": {
                              "comments": "Ava Chen",
                              "description": "Ava Chen",
                              "examples": [
                                "Ava Chen"
                              ],
                              "maxLength": 1,
                              "minLength": 1,
                              "title": "Ava Chen",
                              "type": "Ava Chen"
                            },
                            "materialPercentage": {
                              "comments": "string",
                              "description": "string",
                              "examples": [
                                "string"
                              ],
                              "maximum": 1,
                              "minimum": 1,
                              "multipleOf": 1,
                              "title": "string",
                              "type": "string"
                            }
                          },
                          "required": [
                            "string"
                          ],
                          "type": "string"
                        },
                        "minItems": 1,
                        "title": "string",
                        "type": "string"
                      },
                      "features": {
                        "$schema": "string",
                        "comments": "string",
                        "description": "string",
                        "examples": "string",
                        "items": {
                          "enum": [
                            "string"
                          ],
                          "type": "string"
                        },
                        "minItems": 1,
                        "title": "string",
                        "type": "string"
                      },
                      "frameColorConfiguration": {
                        "$schema": "string",
                        "comments": "string",
                        "description": "string",
                        "examples": [
                          "string"
                        ],
                        "items": {
                          "maxLength": 1,
                          "minLength": 1,
                          "type": "string"
                        },
                        "minItems": 1,
                        "title": "string",
                        "type": "string"
                      },
                      "frontEndPhotoPartner": {
                        "comments": "string",
                        "description": "string",
                        "enum": [
                          "string"
                        ],
                        "examples": "string",
                        "title": "string",
                        "type": "string"
                      },
                      "gender": {
                        "comments": "string",
                        "description": "string",
                        "enum": [
                          "string"
                        ],
                        "examples": "string",
                        "title": "string",
                        "type": "string"
                      },
                      "globalBrandLicense": {
                        "$schema": "string",
                        "comments": "string",
                        "description": "string",
                        "examples": [
                          "string"
                        ],
                        "items": {
                          "maxLength": 1,
                          "minLength": 1,
                          "type": "string"
                        },
                        "minItems": 1,
                        "title": "string",
                        "type": "string"
                      },
                      "gramsPerSquareMeterGsm": {
                        "$schema": "string",
                        "additionalProperties": true,
                        "comments": "string",
                        "description": "string",
                        "examples": [
                          "string"
                        ],
                        "properties": {
                          "measure": {
                            "comments": "string",
                            "description": "string",
                            "examples": [
                              "string"
                            ],
                            "maximum": 1,
                            "minimum": 1,
                            "title": "string",
                            "type": "string"
                          },
                          "unit": {
                            "comments": "string",
                            "description": "string",
                            "enum": [
                              "string"
                            ],
                            "examples": [
                              "string"
                            ],
                            "title": "string",
                            "type": "string"
                          }
                        },
                        "required": [
                          "string"
                        ],
                        "title": "string",
                        "type": "string"
                      },
                      "hasWrittenWarranty": {
                        "comments": "string",
                        "description": "string",
                        "enum": [
                          "string"
                        ],
                        "examples": "string",
                        "title": "string",
                        "type": "string"
                      },
                      "homeDecorStyle": {
                        "$schema": "string",
                        "comments": "string",
                        "description": "string",
                        "examples": "string",
                        "items": {
                          "enum": [
                            "string"
                          ],
                          "type": "string"
                        },
                        "minItems": 1,
                        "title": "string",
                        "type": "string"
                      },
                      "ibBlanketStyle": {
                        "comments": "string",
                        "description": "string",
                        "enum": [
                          "string"
                        ],
                        "examples": "string",
                        "title": "string",
                        "type": "string"
                      },
                      "isPrimaryVariant": {
                        "comments": "string",
                        "description": "string",
                        "enum": [
                          "string"
                        ],
                        "examples": "string",
                        "title": "string",
                        "type": "string"
                      },
                      "isProp65WarningRequired": {
                        "comments": "string",
                        "description": "string",
                        "enum": [
                          "string"
                        ],
                        "examples": "string",
                        "title": "string",
                        "type": "string"
                      },
                      "keyFeatures": {
                        "$schema": "string",
                        "comments": "string",
                        "description": "string",
                        "examples": [
                          "string"
                        ],
                        "items": {
                          "maxLength": 1,
                          "minLength": 1,
                          "type": "string"
                        },
                        "minItems": 1,
                        "title": "string",
                        "type": "string"
                      },
                      "lawLabelDisclosure": {
                        "$schema": "string",
                        "additionalProperties": true,
                        "comments": "string",
                        "description": "string",
                        "examples": "string",
                        "properties": {
                          "lawLabelIdentificationProvider": {
                            "comments": "string",
                            "description": "string",
                            "enum": [
                              "string"
                            ],
                            "examples": "string",
                            "title": "string",
                            "type": "string"
                          },
                          "lawLabelRegistrationNumber": {
                            "comments": "string",
                            "description": "string",
                            "examples": "string",
                            "maxLength": 1,
                            "minLength": 1,
                            "title": "string",
                            "type": "string"
                          }
                        },
                        "required": [
                          "string"
                        ],
                        "title": "string",
                        "type": "string"
                      },
                      "mainImageUrl": {
                        "comments": "https://example.com",
                        "description": "https://example.com",
                        "examples": "https://example.com",
                        "format": "https://example.com",
                        "maxLength": 1,
                        "minLength": 1,
                        "title": "https://example.com",
                        "type": "https://example.com"
                      },
                      "manufacturer": {
                        "comments": "string",
                        "description": "string",
                        "examples": [
                          "string"
                        ],
                        "maxLength": 1,
                        "minLength": 1,
                        "title": "string",
                        "type": "string"
                      },
                      "manufacturerPartNumber": {
                        "comments": "string",
                        "description": "string",
                        "examples": [
                          "string"
                        ],
                        "maxLength": 1,
                        "minLength": 1,
                        "title": "string",
                        "type": "string"
                      },
                      "maximumOrderQuantity": {
                        "comments": "string",
                        "description": "string",
                        "examples": [
                          "string"
                        ],
                        "maximum": 1,
                        "minimum": 1,
                        "title": "string",
                        "type": "string"
                      },
                      "minimumOrderQuantity": {
                        "comments": "string",
                        "description": "string",
                        "examples": [
                          "string"
                        ],
                        "maximum": 1,
                        "minimum": 1,
                        "title": "string",
                        "type": "string"
                      },
                      "modelNumber": {
                        "comments": "string",
                        "description": "string",
                        "examples": [
                          "string"
                        ],
                        "maxLength": 1,
                        "minLength": 1,
                        "title": "string",
                        "type": "string"
                      },
                      "multipackQuantity": {
                        "comments": "string",
                        "description": "string",
                        "examples": [
                          "string"
                        ],
                        "maximum": 1,
                        "minimum": 1,
                        "title": "string",
                        "type": "string"
                      },
                      "netContent": {
                        "$schema": "string",
                        "additionalProperties": true,
                        "comments": "string",
                        "description": "string",
                        "examples": "string",
                        "properties": {
                          "productNetContentMeasure": {
                            "comments": "string",
                            "description": "string",
                            "examples": [
                              "string"
                            ],
                            "maximum": 1,
                            "minimum": 1,
                            "multipleOf": 1,
                            "title": "string",
                            "type": "string"
                          },
                          "productNetContentUnit": {
                            "comments": "string",
                            "description": "string",
                            "enum": [
                              "string"
                            ],
                            "examples": "string",
                            "title": "string",
                            "type": "string"
                          }
                        },
                        "required": [
                          "string"
                        ],
                        "title": "string",
                        "type": "string"
                      },
                      "netContentStatement": {
                        "comments": "string",
                        "description": "string",
                        "examples": [
                          "string"
                        ],
                        "maxLength": 1,
                        "minLength": 1,
                        "title": "string",
                        "type": "string"
                      },
                      "occasion": {
                        "$schema": "string",
                        "comments": "string",
                        "description": "string",
                        "examples": [
                          "string"
                        ],
                        "items": {
                          "maxLength": 1,
                          "minLength": 1,
                          "type": "string"
                        },
                        "minItems": 1,
                        "title": "string",
                        "type": "string"
                      },
                      "pattern": {
                        "$schema": "string",
                        "comments": "string",
                        "description": "string",
                        "examples": [
                          "string"
                        ],
                        "items": {
                          "maxLength": 1,
                          "minLength": 1,
                          "type": "string"
                        },
                        "minItems": 1,
                        "title": "string",
                        "type": "string"
                      },
                      "photoAccessoryItemSku": {
                        "$schema": "string",
                        "comments": "string",
                        "description": "string",
                        "examples": [
                          "string"
                        ],
                        "items": {
                          "maxLength": 1,
                          "minLength": 1,
                          "type": "string"
                        },
                        "minItems": 1,
                        "title": "string",
                        "type": "string"
                      },
                      "photoConfigurationAttributeNames": {
                        "$schema": "Ava Chen",
                        "comments": "Ava Chen",
                        "description": "Ava Chen",
                        "examples": "Ava Chen",
                        "items": {
                          "enum": [
                            "Ava Chen"
                          ],
                          "type": "Ava Chen"
                        },
                        "minItems": 1,
                        "title": "Ava Chen",
                        "type": "Ava Chen"
                      },
                      "photoItemStoreUpc": {
                        "comments": "string",
                        "description": "string",
                        "examples": [
                          "string"
                        ],
                        "maxLength": 1,
                        "minLength": 1,
                        "title": "string",
                        "type": "string"
                      },
                      "photoOrderQuantityTier": {
                        "comments": "string",
                        "description": "string",
                        "examples": [
                          "string"
                        ],
                        "maximum": 1,
                        "minimum": 1,
                        "title": "string",
                        "type": "string"
                      },
                      "photoPaperFinishConfiguration": {
                        "$schema": "string",
                        "comments": "string",
                        "description": "string",
                        "examples": "string",
                        "items": {
                          "enum": [
                            "string"
                          ],
                          "type": "string"
                        },
                        "minItems": 1,
                        "title": "string",
                        "type": "string"
                      },
                      "pieceCount": {
                        "comments": "string",
                        "description": "string",
                        "examples": [
                          "string"
                        ],
                        "maximum": 1,
                        "minimum": 1,
                        "title": "string",
                        "type": "string"
                      },
                      "productLine": {
                        "$schema": "string",
                        "comments": "string",
                        "description": "string",
                        "examples": [
                          "string"
                        ],
                        "items": {
                          "maxLength": 1,
                          "minLength": 1,
                          "type": "string"
                        },
                        "minItems": 1,
                        "title": "string",
                        "type": "string"
                      },
                      "productName": {
                        "comments": "Ava Chen",
                        "description": "Ava Chen",
                        "examples": [
                          "Ava Chen"
                        ],
                        "maxLength": 1,
                        "minLength": 1,
                        "title": "Ava Chen",
                        "type": "Ava Chen"
                      },
                      "productSecondaryImageURL": {
                        "$schema": "https://example.com",
                        "comments": "https://example.com",
                        "description": "https://example.com",
                        "examples": "https://example.com",
                        "items": {
                          "format": "https://example.com",
                          "maxLength": 1,
                          "minLength": 1,
                          "type": "https://example.com"
                        },
                        "minItems": 1,
                        "title": "https://example.com",
                        "type": "https://example.com"
                      },
                      "prop65WarningText": {
                        "comments": "string",
                        "description": "string",
                        "examples": [
                          "string"
                        ],
                        "maxLength": 1,
                        "minLength": 1,
                        "title": "string",
                        "type": "string"
                      },
                      "shortDescription": {
                        "comments": "string",
                        "description": "string",
                        "examples": [
                          "string"
                        ],
                        "maxLength": 1,
                        "minLength": 1,
                        "title": "string",
                        "type": "string"
                      },
                      "size": {
                        "comments": "string",
                        "description": "string",
                        "examples": [
                          "string"
                        ],
                        "maxLength": 1,
                        "minLength": 1,
                        "title": "string",
                        "type": "string"
                      },
                      "smallPartsWarnings": {
                        "$schema": "string",
                        "comments": "string",
                        "description": "string",
                        "examples": "string",
                        "items": {
                          "enum": [
                            "string"
                          ],
                          "type": "string"
                        },
                        "minItems": 1,
                        "title": "string",
                        "type": "string"
                      },
                      "sportsLeague": {
                        "$schema": "string",
                        "comments": "string",
                        "description": "string",
                        "examples": [
                          "string"
                        ],
                        "items": {
                          "maxLength": 1,
                          "minLength": 1,
                          "type": "string"
                        },
                        "minItems": 1,
                        "title": "string",
                        "type": "string"
                      },
                      "sportsTeam": {
                        "$schema": "string",
                        "comments": "string",
                        "description": "string",
                        "examples": [
                          "string"
                        ],
                        "items": {
                          "maxLength": 1,
                          "minLength": 1,
                          "type": "string"
                        },
                        "minItems": 1,
                        "title": "string",
                        "type": "string"
                      },
                      "swatchImages": {
                        "$schema": "string",
                        "comments": "string",
                        "description": "string",
                        "examples": "string",
                        "items": {
                          "$schema": "string",
                          "additionalProperties": true,
                          "properties": {
                            "swatchImageUrl": {
                              "comments": "https://example.com",
                              "description": "https://example.com",
                              "examples": [
                                "https://example.com"
                              ],
                              "format": "https://example.com",
                              "maxLength": 1,
                              "minLength": 1,
                              "title": "https://example.com",
                              "type": "https://example.com"
                            },
                            "swatchVariantAttribute": {
                              "comments": "string",
                              "description": "string",
                              "enum": [
                                "string"
                              ],
                              "examples": "string",
                              "title": "string",
                              "type": "string"
                            }
                          },
                          "type": "string"
                        },
                        "minItems": 1,
                        "title": "string",
                        "type": "string"
                      },
                      "theme": {
                        "comments": "string",
                        "description": "string",
                        "examples": [
                          "string"
                        ],
                        "maxLength": 1,
                        "minLength": 1,
                        "title": "string",
                        "type": "string"
                      },
                      "thirdPartyAccreditationSymbolOnProductPackageCode": {
                        "$schema": "string",
                        "comments": "string",
                        "description": "string",
                        "examples": "string",
                        "items": {
                          "enum": [
                            "string"
                          ],
                          "type": "string"
                        },
                        "minItems": 1,
                        "title": "string",
                        "type": "string"
                      },
                      "threadCount": {
                        "comments": "string",
                        "description": "string",
                        "examples": [
                          "string"
                        ],
                        "maximum": 1,
                        "minimum": 1,
                        "title": "string",
                        "type": "string"
                      },
                      "variantAttributeNames": {
                        "$schema": "Ava Chen",
                        "comments": "Ava Chen",
                        "description": "Ava Chen",
                        "examples": "Ava Chen",
                        "items": {
                          "enum": [
                            "Ava Chen"
                          ],
                          "type": "Ava Chen"
                        },
                        "minItems": 1,
                        "title": "Ava Chen",
                        "type": "Ava Chen"
                      },
                      "variantGroupId": {
                        "comments": "string",
                        "description": "string",
                        "examples": [
                          "string"
                        ],
                        "maxLength": 1,
                        "minLength": 1,
                        "title": "string",
                        "type": "string"
                      },
                      "warrantyText": {
                        "comments": "string",
                        "description": "string",
                        "examples": [
                          "string"
                        ],
                        "maxLength": 1,
                        "minLength": 1,
                        "title": "string",
                        "type": "string"
                      },
                      "warrantyURL": {
                        "comments": "https://example.com",
                        "description": "https://example.com",
                        "examples": [
                          "https://example.com"
                        ],
                        "format": "https://example.com",
                        "maxLength": 1,
                        "minLength": 1,
                        "title": "https://example.com",
                        "type": "https://example.com"
                      },
                      "weavingTechnique": {
                        "comments": "string",
                        "description": "string",
                        "examples": [
                          "string"
                        ],
                        "maxLength": 1,
                        "minLength": 1,
                        "title": "string",
                        "type": "string"
                      }
                    },
                    "required": [
                      "string"
                    ],
                    "type": "string"
                  }
                },
                "title": "string",
                "type": "string"
              }
            },
            "required": [
              "string"
            ],
            "type": "string"
          },
          "minItems": 1,
          "title": "string",
          "type": "string"
        },
        "mPItemFeedHeader": {
          "$schema": "string",
          "additionalProperties": true,
          "properties": {
            "businessUnit": {
              "enum": [
                "string"
              ],
              "title": "string",
              "type": "string"
            },
            "locale": {
              "enum": [
                "string"
              ],
              "title": "string",
              "type": "string"
            },
            "version": {
              "enum": [
                "string"
              ],
              "title": "string",
              "type": "string"
            }
          },
          "required": [
            "string"
          ],
          "title": "string",
          "type": "string"
        }
      },
      "required": [
        "string"
      ],
      "title": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `$schema` | string |  |
| `additionalProperties` | boolean |  |
| `properties.mPItem.$schema` | string |  |
| `properties.mPItem.items.$schema` | string |  |
| `properties.mPItem.items.additionalProperties` | boolean |  |
| `properties.mPItem.items.properties.orderable.$schema` | string |  |
| `properties.mPItem.items.properties.orderable.additionalProperties` | boolean |  |
| `properties.mPItem.items.properties.orderable.allOf[].if.anyOf[].properties.chemicalAerosolPesticide.enum[]` | string |  |
| `properties.mPItem.items.properties.orderable.allOf[].if.anyOf[].properties.chemicalAerosolPesticide.type` | string |  |
| `properties.mPItem.items.properties.orderable.allOf[].if.anyOf[].required[]` | string |  |
| `properties.mPItem.items.properties.orderable.allOf[].then.required[]` | string |  |
| `properties.mPItem.items.properties.orderable.properties.batterySize.comments` | string |  |
| `properties.mPItem.items.properties.orderable.properties.batterySize.description` | string |  |
| `properties.mPItem.items.properties.orderable.properties.batterySize.enum[]` | string |  |
| `properties.mPItem.items.properties.orderable.properties.batterySize.examples` | string |  |
| `properties.mPItem.items.properties.orderable.properties.batterySize.title` | string |  |
| `properties.mPItem.items.properties.orderable.properties.batterySize.type` | string |  |
| `properties.mPItem.items.properties.orderable.properties.batteryTechnologyType.comments` | string |  |
| `properties.mPItem.items.properties.orderable.properties.batteryTechnologyType.description` | string |  |
| `properties.mPItem.items.properties.orderable.properties.batteryTechnologyType.enum[]` | string |  |
| `properties.mPItem.items.properties.orderable.properties.batteryTechnologyType.examples` | string |  |
| `properties.mPItem.items.properties.orderable.properties.batteryTechnologyType.title` | string |  |
| `properties.mPItem.items.properties.orderable.properties.batteryTechnologyType.type` | string |  |
| `properties.mPItem.items.properties.orderable.properties.chemicalAerosolPesticide.comments` | string |  |
| `properties.mPItem.items.properties.orderable.properties.chemicalAerosolPesticide.description` | string |  |
| `properties.mPItem.items.properties.orderable.properties.chemicalAerosolPesticide.enum[]` | string |  |
| `properties.mPItem.items.properties.orderable.properties.chemicalAerosolPesticide.examples` | string |  |
| `properties.mPItem.items.properties.orderable.properties.chemicalAerosolPesticide.title` | string |  |
| `properties.mPItem.items.properties.orderable.properties.chemicalAerosolPesticide.type` | string |  |
| `properties.mPItem.items.properties.orderable.properties.electronicsIndicator.comments` | string |  |
| `properties.mPItem.items.properties.orderable.properties.electronicsIndicator.description` | string |  |
| `properties.mPItem.items.properties.orderable.properties.electronicsIndicator.enum[]` | string |  |
| `properties.mPItem.items.properties.orderable.properties.electronicsIndicator.examples` | string |  |
| `properties.mPItem.items.properties.orderable.properties.electronicsIndicator.title` | string |  |
| `properties.mPItem.items.properties.orderable.properties.electronicsIndicator.type` | string |  |
| `properties.mPItem.items.properties.orderable.properties.endDate.comments` | string |  |
| `properties.mPItem.items.properties.orderable.properties.endDate.description` | string |  |
| `properties.mPItem.items.properties.orderable.properties.endDate.examples[]` | string |  |
| `properties.mPItem.items.properties.orderable.properties.endDate.format` | string |  |
| `properties.mPItem.items.properties.orderable.properties.endDate.title` | string |  |
| `properties.mPItem.items.properties.orderable.properties.endDate.type` | string |  |
| `properties.mPItem.items.properties.orderable.properties.externalProductIdentifier.$schema` | string |  |
| `properties.mPItem.items.properties.orderable.properties.externalProductIdentifier.comments` | string |  |
| `properties.mPItem.items.properties.orderable.properties.externalProductIdentifier.description` | string |  |
| `properties.mPItem.items.properties.orderable.properties.externalProductIdentifier.examples` | string |  |
| `properties.mPItem.items.properties.orderable.properties.externalProductIdentifier.items.$schema` | string |  |
| `properties.mPItem.items.properties.orderable.properties.externalProductIdentifier.items.additionalProperties` | boolean |  |
| `properties.mPItem.items.properties.orderable.properties.externalProductIdentifier.items.properties.externalProductId.comments` | string |  |
| `properties.mPItem.items.properties.orderable.properties.externalProductIdentifier.items.properties.externalProductId.description` | string |  |
| `properties.mPItem.items.properties.orderable.properties.externalProductIdentifier.items.properties.externalProductId.examples[]` | string |  |
| `properties.mPItem.items.properties.orderable.properties.externalProductIdentifier.items.properties.externalProductId.maxLength` | number |  |
| `properties.mPItem.items.properties.orderable.properties.externalProductIdentifier.items.properties.externalProductId.minLength` | number |  |
| `properties.mPItem.items.properties.orderable.properties.externalProductIdentifier.items.properties.externalProductId.title` | string |  |
| `properties.mPItem.items.properties.orderable.properties.externalProductIdentifier.items.properties.externalProductId.type` | string |  |
| `properties.mPItem.items.properties.orderable.properties.externalProductIdentifier.items.properties.externalProductIdType.comments` | string |  |
| `properties.mPItem.items.properties.orderable.properties.externalProductIdentifier.items.properties.externalProductIdType.description` | string |  |
| `properties.mPItem.items.properties.orderable.properties.externalProductIdentifier.items.properties.externalProductIdType.enum[]` | string |  |
| `properties.mPItem.items.properties.orderable.properties.externalProductIdentifier.items.properties.externalProductIdType.examples` | string |  |
| `properties.mPItem.items.properties.orderable.properties.externalProductIdentifier.items.properties.externalProductIdType.title` | string |  |
| `properties.mPItem.items.properties.orderable.properties.externalProductIdentifier.items.properties.externalProductIdType.type` | string |  |
| `properties.mPItem.items.properties.orderable.properties.externalProductIdentifier.items.required[]` | string |  |
| `properties.mPItem.items.properties.orderable.properties.externalProductIdentifier.items.type` | string |  |
| `properties.mPItem.items.properties.orderable.properties.externalProductIdentifier.minItems` | number |  |
| `properties.mPItem.items.properties.orderable.properties.externalProductIdentifier.title` | string |  |
| `properties.mPItem.items.properties.orderable.properties.externalProductIdentifier.type` | string |  |
| `properties.mPItem.items.properties.orderable.properties.hasBatteries.comments` | string |  |
| `properties.mPItem.items.properties.orderable.properties.hasBatteries.description` | string |  |
| `properties.mPItem.items.properties.orderable.properties.hasBatteries.enum[]` | string |  |
| `properties.mPItem.items.properties.orderable.properties.hasBatteries.examples` | string |  |
| `properties.mPItem.items.properties.orderable.properties.hasBatteries.title` | string |  |
| `properties.mPItem.items.properties.orderable.properties.hasBatteries.type` | string |  |
| `properties.mPItem.items.properties.orderable.properties.labelImage.$schema` | string |  |
| `properties.mPItem.items.properties.orderable.properties.labelImage.comments` | string |  |
| `properties.mPItem.items.properties.orderable.properties.labelImage.description` | string |  |
| `properties.mPItem.items.properties.orderable.properties.labelImage.examples` | string |  |
| `properties.mPItem.items.properties.orderable.properties.labelImage.items.$schema` | string |  |
| `properties.mPItem.items.properties.orderable.properties.labelImage.items.additionalProperties` | boolean |  |
| `properties.mPItem.items.properties.orderable.properties.labelImage.items.properties.labelImageContains.comments` | string |  |
| `properties.mPItem.items.properties.orderable.properties.labelImage.items.properties.labelImageContains.description` | string |  |
| `properties.mPItem.items.properties.orderable.properties.labelImage.items.properties.labelImageContains.enum[]` | string |  |
| `properties.mPItem.items.properties.orderable.properties.labelImage.items.properties.labelImageContains.examples` | string |  |
| `properties.mPItem.items.properties.orderable.properties.labelImage.items.properties.labelImageContains.title` | string |  |
| `properties.mPItem.items.properties.orderable.properties.labelImage.items.properties.labelImageContains.type` | string |  |
| `properties.mPItem.items.properties.orderable.properties.labelImage.items.properties.labelImageURL.comments` | string |  |
| `properties.mPItem.items.properties.orderable.properties.labelImage.items.properties.labelImageURL.description` | string |  |
| `properties.mPItem.items.properties.orderable.properties.labelImage.items.properties.labelImageURL.examples[]` | string |  |
| `properties.mPItem.items.properties.orderable.properties.labelImage.items.properties.labelImageURL.format` | string |  |
| `properties.mPItem.items.properties.orderable.properties.labelImage.items.properties.labelImageURL.maxLength` | number |  |
| `properties.mPItem.items.properties.orderable.properties.labelImage.items.properties.labelImageURL.minLength` | number |  |
| `properties.mPItem.items.properties.orderable.properties.labelImage.items.properties.labelImageURL.title` | string |  |
| `properties.mPItem.items.properties.orderable.properties.labelImage.items.properties.labelImageURL.type` | string |  |
| `properties.mPItem.items.properties.orderable.properties.labelImage.items.type` | string |  |
| `properties.mPItem.items.properties.orderable.properties.labelImage.minItems` | number |  |
| `properties.mPItem.items.properties.orderable.properties.labelImage.title` | string |  |
| `properties.mPItem.items.properties.orderable.properties.labelImage.type` | string |  |
| `properties.mPItem.items.properties.orderable.properties.lithiumIonBatteries.$schema` | string |  |
| `properties.mPItem.items.properties.orderable.properties.lithiumIonBatteries.additionalProperties` | boolean |  |
| `properties.mPItem.items.properties.orderable.properties.lithiumIonBatteries.comments` | string |  |
| `properties.mPItem.items.properties.orderable.properties.lithiumIonBatteries.description` | string |  |
| `properties.mPItem.items.properties.orderable.properties.lithiumIonBatteries.examples` | string |  |
| `properties.mPItem.items.properties.orderable.properties.lithiumIonBatteries.properties.batteryWattHour.comments` | string |  |
| `properties.mPItem.items.properties.orderable.properties.lithiumIonBatteries.properties.batteryWattHour.description` | string |  |
| `properties.mPItem.items.properties.orderable.properties.lithiumIonBatteries.properties.batteryWattHour.examples` | string |  |
| `properties.mPItem.items.properties.orderable.properties.lithiumIonBatteries.properties.batteryWattHour.maximum` | number |  |
| `properties.mPItem.items.properties.orderable.properties.lithiumIonBatteries.properties.batteryWattHour.minimum` | number |  |
| `properties.mPItem.items.properties.orderable.properties.lithiumIonBatteries.properties.batteryWattHour.multipleOf` | number |  |
| `properties.mPItem.items.properties.orderable.properties.lithiumIonBatteries.properties.batteryWattHour.title` | string |  |
| `properties.mPItem.items.properties.orderable.properties.lithiumIonBatteries.properties.batteryWattHour.type` | string |  |
| `properties.mPItem.items.properties.orderable.properties.lithiumIonBatteries.properties.ionBatteryFormFactor.comments` | string |  |
| `properties.mPItem.items.properties.orderable.properties.lithiumIonBatteries.properties.ionBatteryFormFactor.description` | string |  |
| `properties.mPItem.items.properties.orderable.properties.lithiumIonBatteries.properties.ionBatteryFormFactor.enum[]` | string |  |
| `properties.mPItem.items.properties.orderable.properties.lithiumIonBatteries.properties.ionBatteryFormFactor.examples` | string |  |
| `properties.mPItem.items.properties.orderable.properties.lithiumIonBatteries.properties.ionBatteryFormFactor.title` | string |  |
| `properties.mPItem.items.properties.orderable.properties.lithiumIonBatteries.properties.ionBatteryFormFactor.type` | string |  |
| `properties.mPItem.items.properties.orderable.properties.lithiumIonBatteries.properties.ionBatteryModel.comments` | string |  |
| `properties.mPItem.items.properties.orderable.properties.lithiumIonBatteries.properties.ionBatteryModel.description` | string |  |
| `properties.mPItem.items.properties.orderable.properties.lithiumIonBatteries.properties.ionBatteryModel.examples[]` | string |  |
| `properties.mPItem.items.properties.orderable.properties.lithiumIonBatteries.properties.ionBatteryModel.maxLength` | number |  |
| `properties.mPItem.items.properties.orderable.properties.lithiumIonBatteries.properties.ionBatteryModel.minLength` | number |  |
| `properties.mPItem.items.properties.orderable.properties.lithiumIonBatteries.properties.ionBatteryModel.title` | string |  |
| `properties.mPItem.items.properties.orderable.properties.lithiumIonBatteries.properties.ionBatteryModel.type` | string |  |
| `properties.mPItem.items.properties.orderable.properties.lithiumIonBatteries.properties.ionBatteryWeight.comments` | string |  |
| `properties.mPItem.items.properties.orderable.properties.lithiumIonBatteries.properties.ionBatteryWeight.description` | string |  |
| `properties.mPItem.items.properties.orderable.properties.lithiumIonBatteries.properties.ionBatteryWeight.examples[]` | string |  |
| `properties.mPItem.items.properties.orderable.properties.lithiumIonBatteries.properties.ionBatteryWeight.maximum` | number |  |
| `properties.mPItem.items.properties.orderable.properties.lithiumIonBatteries.properties.ionBatteryWeight.minimum` | number |  |
| `properties.mPItem.items.properties.orderable.properties.lithiumIonBatteries.properties.ionBatteryWeight.multipleOf` | number |  |
| `properties.mPItem.items.properties.orderable.properties.lithiumIonBatteries.properties.ionBatteryWeight.title` | string |  |
| `properties.mPItem.items.properties.orderable.properties.lithiumIonBatteries.properties.ionBatteryWeight.type` | string |  |
| `properties.mPItem.items.properties.orderable.properties.lithiumIonBatteries.properties.ionIncludedBatteryPackaging.comments` | string |  |
| `properties.mPItem.items.properties.orderable.properties.lithiumIonBatteries.properties.ionIncludedBatteryPackaging.description` | string |  |
| `properties.mPItem.items.properties.orderable.properties.lithiumIonBatteries.properties.ionIncludedBatteryPackaging.enum[]` | string |  |
| `properties.mPItem.items.properties.orderable.properties.lithiumIonBatteries.properties.ionIncludedBatteryPackaging.examples` | string |  |
| `properties.mPItem.items.properties.orderable.properties.lithiumIonBatteries.properties.ionIncludedBatteryPackaging.title` | string |  |
| `properties.mPItem.items.properties.orderable.properties.lithiumIonBatteries.properties.ionIncludedBatteryPackaging.type` | string |  |
| `properties.mPItem.items.properties.orderable.properties.lithiumIonBatteries.properties.ionNumberOfBatteries.comments` | string |  |
| `properties.mPItem.items.properties.orderable.properties.lithiumIonBatteries.properties.ionNumberOfBatteries.description` | string |  |
| `properties.mPItem.items.properties.orderable.properties.lithiumIonBatteries.properties.ionNumberOfBatteries.examples[]` | string |  |
| `properties.mPItem.items.properties.orderable.properties.lithiumIonBatteries.properties.ionNumberOfBatteries.maximum` | number |  |
| `properties.mPItem.items.properties.orderable.properties.lithiumIonBatteries.properties.ionNumberOfBatteries.minimum` | number |  |
| `properties.mPItem.items.properties.orderable.properties.lithiumIonBatteries.properties.ionNumberOfBatteries.title` | string |  |
| `properties.mPItem.items.properties.orderable.properties.lithiumIonBatteries.properties.ionNumberOfBatteries.type` | string |  |
| `properties.mPItem.items.properties.orderable.properties.lithiumIonBatteries.properties.ionNumberOfBatteryCells.comments` | string |  |
| `properties.mPItem.items.properties.orderable.properties.lithiumIonBatteries.properties.ionNumberOfBatteryCells.description` | string |  |
| `properties.mPItem.items.properties.orderable.properties.lithiumIonBatteries.properties.ionNumberOfBatteryCells.examples[]` | string |  |
| `properties.mPItem.items.properties.orderable.properties.lithiumIonBatteries.properties.ionNumberOfBatteryCells.maximum` | number |  |
| `properties.mPItem.items.properties.orderable.properties.lithiumIonBatteries.properties.ionNumberOfBatteryCells.minimum` | number |  |
| `properties.mPItem.items.properties.orderable.properties.lithiumIonBatteries.properties.ionNumberOfBatteryCells.title` | string |  |
| `properties.mPItem.items.properties.orderable.properties.lithiumIonBatteries.properties.ionNumberOfBatteryCells.type` | string |  |
| `properties.mPItem.items.properties.orderable.properties.lithiumIonBatteries.required[]` | string |  |
| `properties.mPItem.items.properties.orderable.properties.lithiumIonBatteries.title` | string |  |
| `properties.mPItem.items.properties.orderable.properties.lithiumIonBatteries.type` | string |  |
| `properties.mPItem.items.properties.orderable.properties.lithiumMetalBatteries.$schema` | string |  |
| `properties.mPItem.items.properties.orderable.properties.lithiumMetalBatteries.additionalProperties` | boolean |  |
| `properties.mPItem.items.properties.orderable.properties.lithiumMetalBatteries.comments` | string |  |
| `properties.mPItem.items.properties.orderable.properties.lithiumMetalBatteries.description` | string |  |
| `properties.mPItem.items.properties.orderable.properties.lithiumMetalBatteries.examples` | string |  |
| `properties.mPItem.items.properties.orderable.properties.lithiumMetalBatteries.properties.lithiumMetalContentWeight.comments` | string |  |
| `properties.mPItem.items.properties.orderable.properties.lithiumMetalBatteries.properties.lithiumMetalContentWeight.description` | string |  |
| `properties.mPItem.items.properties.orderable.properties.lithiumMetalBatteries.properties.lithiumMetalContentWeight.examples` | string |  |
| `properties.mPItem.items.properties.orderable.properties.lithiumMetalBatteries.properties.lithiumMetalContentWeight.maximum` | number |  |
| `properties.mPItem.items.properties.orderable.properties.lithiumMetalBatteries.properties.lithiumMetalContentWeight.minimum` | number |  |
| `properties.mPItem.items.properties.orderable.properties.lithiumMetalBatteries.properties.lithiumMetalContentWeight.multipleOf` | number |  |
| `properties.mPItem.items.properties.orderable.properties.lithiumMetalBatteries.properties.lithiumMetalContentWeight.title` | string |  |
| `properties.mPItem.items.properties.orderable.properties.lithiumMetalBatteries.properties.lithiumMetalContentWeight.type` | string |  |
| `properties.mPItem.items.properties.orderable.properties.lithiumMetalBatteries.properties.metalBatteryCellCount.comments` | string |  |
| `properties.mPItem.items.properties.orderable.properties.lithiumMetalBatteries.properties.metalBatteryCellCount.description` | string |  |
| `properties.mPItem.items.properties.orderable.properties.lithiumMetalBatteries.properties.metalBatteryCellCount.examples[]` | string |  |
| `properties.mPItem.items.properties.orderable.properties.lithiumMetalBatteries.properties.metalBatteryCellCount.maximum` | number |  |
| `properties.mPItem.items.properties.orderable.properties.lithiumMetalBatteries.properties.metalBatteryCellCount.minimum` | number |  |
| `properties.mPItem.items.properties.orderable.properties.lithiumMetalBatteries.properties.metalBatteryCellCount.title` | string |  |
| `properties.mPItem.items.properties.orderable.properties.lithiumMetalBatteries.properties.metalBatteryCellCount.type` | string |  |
| `properties.mPItem.items.properties.orderable.properties.lithiumMetalBatteries.properties.metalBatteryFormFactor.comments` | string |  |
| `properties.mPItem.items.properties.orderable.properties.lithiumMetalBatteries.properties.metalBatteryFormFactor.description` | string |  |
| `properties.mPItem.items.properties.orderable.properties.lithiumMetalBatteries.properties.metalBatteryFormFactor.enum[]` | string |  |
| `properties.mPItem.items.properties.orderable.properties.lithiumMetalBatteries.properties.metalBatteryFormFactor.examples` | string |  |
| `properties.mPItem.items.properties.orderable.properties.lithiumMetalBatteries.properties.metalBatteryFormFactor.title` | string |  |
| `properties.mPItem.items.properties.orderable.properties.lithiumMetalBatteries.properties.metalBatteryFormFactor.type` | string |  |
| `properties.mPItem.items.properties.orderable.properties.lithiumMetalBatteries.properties.metalBatteryModel.comments` | string |  |
| `properties.mPItem.items.properties.orderable.properties.lithiumMetalBatteries.properties.metalBatteryModel.description` | string |  |
| `properties.mPItem.items.properties.orderable.properties.lithiumMetalBatteries.properties.metalBatteryModel.examples[]` | string |  |
| `properties.mPItem.items.properties.orderable.properties.lithiumMetalBatteries.properties.metalBatteryModel.maxLength` | number |  |
| `properties.mPItem.items.properties.orderable.properties.lithiumMetalBatteries.properties.metalBatteryModel.minLength` | number |  |
| `properties.mPItem.items.properties.orderable.properties.lithiumMetalBatteries.properties.metalBatteryModel.title` | string |  |
| `properties.mPItem.items.properties.orderable.properties.lithiumMetalBatteries.properties.metalBatteryModel.type` | string |  |
| `properties.mPItem.items.properties.orderable.properties.lithiumMetalBatteries.properties.metalBatteryWeight.comments` | string |  |
| `properties.mPItem.items.properties.orderable.properties.lithiumMetalBatteries.properties.metalBatteryWeight.description` | string |  |
| `properties.mPItem.items.properties.orderable.properties.lithiumMetalBatteries.properties.metalBatteryWeight.examples[]` | string |  |
| `properties.mPItem.items.properties.orderable.properties.lithiumMetalBatteries.properties.metalBatteryWeight.maximum` | number |  |
| `properties.mPItem.items.properties.orderable.properties.lithiumMetalBatteries.properties.metalBatteryWeight.minimum` | number |  |
| `properties.mPItem.items.properties.orderable.properties.lithiumMetalBatteries.properties.metalBatteryWeight.multipleOf` | number |  |
| `properties.mPItem.items.properties.orderable.properties.lithiumMetalBatteries.properties.metalBatteryWeight.title` | string |  |
| `properties.mPItem.items.properties.orderable.properties.lithiumMetalBatteries.properties.metalBatteryWeight.type` | string |  |
| `properties.mPItem.items.properties.orderable.properties.lithiumMetalBatteries.properties.metalIncludedBatteryPackaging.comments` | string |  |
| `properties.mPItem.items.properties.orderable.properties.lithiumMetalBatteries.properties.metalIncludedBatteryPackaging.description` | string |  |
| `properties.mPItem.items.properties.orderable.properties.lithiumMetalBatteries.properties.metalIncludedBatteryPackaging.enum[]` | string |  |
| `properties.mPItem.items.properties.orderable.properties.lithiumMetalBatteries.properties.metalIncludedBatteryPackaging.examples` | string |  |
| `properties.mPItem.items.properties.orderable.properties.lithiumMetalBatteries.properties.metalIncludedBatteryPackaging.title` | string |  |
| `properties.mPItem.items.properties.orderable.properties.lithiumMetalBatteries.properties.metalIncludedBatteryPackaging.type` | string |  |
| `properties.mPItem.items.properties.orderable.properties.lithiumMetalBatteries.properties.metalNumberOfBatteries.comments` | string |  |
| `properties.mPItem.items.properties.orderable.properties.lithiumMetalBatteries.properties.metalNumberOfBatteries.description` | string |  |
| `properties.mPItem.items.properties.orderable.properties.lithiumMetalBatteries.properties.metalNumberOfBatteries.examples[]` | string |  |
| `properties.mPItem.items.properties.orderable.properties.lithiumMetalBatteries.properties.metalNumberOfBatteries.maximum` | number |  |
| `properties.mPItem.items.properties.orderable.properties.lithiumMetalBatteries.properties.metalNumberOfBatteries.minimum` | number |  |
| `properties.mPItem.items.properties.orderable.properties.lithiumMetalBatteries.properties.metalNumberOfBatteries.title` | string |  |
| `properties.mPItem.items.properties.orderable.properties.lithiumMetalBatteries.properties.metalNumberOfBatteries.type` | string |  |
| `properties.mPItem.items.properties.orderable.properties.lithiumMetalBatteries.required[]` | string |  |
| `properties.mPItem.items.properties.orderable.properties.lithiumMetalBatteries.title` | string |  |
| `properties.mPItem.items.properties.orderable.properties.lithiumMetalBatteries.type` | string |  |
| `properties.mPItem.items.properties.orderable.properties.mustShipAlone.comments` | string |  |
| `properties.mPItem.items.properties.orderable.properties.mustShipAlone.description` | string |  |
| `properties.mPItem.items.properties.orderable.properties.mustShipAlone.enum[]` | string |  |
| `properties.mPItem.items.properties.orderable.properties.mustShipAlone.examples` | string |  |
| `properties.mPItem.items.properties.orderable.properties.mustShipAlone.title` | string |  |
| `properties.mPItem.items.properties.orderable.properties.mustShipAlone.type` | string |  |
| `properties.mPItem.items.properties.orderable.properties.numberOfHazardousComponents.comments` | string |  |
| `properties.mPItem.items.properties.orderable.properties.numberOfHazardousComponents.description` | string |  |
| `properties.mPItem.items.properties.orderable.properties.numberOfHazardousComponents.examples[]` | string |  |
| `properties.mPItem.items.properties.orderable.properties.numberOfHazardousComponents.maximum` | number |  |
| `properties.mPItem.items.properties.orderable.properties.numberOfHazardousComponents.minimum` | number |  |
| `properties.mPItem.items.properties.orderable.properties.numberOfHazardousComponents.title` | string |  |
| `properties.mPItem.items.properties.orderable.properties.numberOfHazardousComponents.type` | string |  |
| `properties.mPItem.items.properties.orderable.properties.price.comments` | string |  |
| `properties.mPItem.items.properties.orderable.properties.price.description` | string |  |
| `properties.mPItem.items.properties.orderable.properties.price.examples[]` | string |  |
| `properties.mPItem.items.properties.orderable.properties.price.maximum` | number |  |
| `properties.mPItem.items.properties.orderable.properties.price.minimum` | number |  |
| `properties.mPItem.items.properties.orderable.properties.price.multipleOf` | number |  |
| `properties.mPItem.items.properties.orderable.properties.price.title` | string |  |
| `properties.mPItem.items.properties.orderable.properties.price.type` | string |  |
| `properties.mPItem.items.properties.orderable.properties.productIdentifiers.$schema` | string |  |
| `properties.mPItem.items.properties.orderable.properties.productIdentifiers.additionalProperties` | boolean |  |
| `properties.mPItem.items.properties.orderable.properties.productIdentifiers.comments` | string |  |
| `properties.mPItem.items.properties.orderable.properties.productIdentifiers.description` | string |  |
| `properties.mPItem.items.properties.orderable.properties.productIdentifiers.examples` | string |  |
| `properties.mPItem.items.properties.orderable.properties.productIdentifiers.properties.productId.comments` | string |  |
| `properties.mPItem.items.properties.orderable.properties.productIdentifiers.properties.productId.description` | string |  |
| `properties.mPItem.items.properties.orderable.properties.productIdentifiers.properties.productId.examples[]` | string |  |
| `properties.mPItem.items.properties.orderable.properties.productIdentifiers.properties.productId.maxLength` | number |  |
| `properties.mPItem.items.properties.orderable.properties.productIdentifiers.properties.productId.minLength` | number |  |
| `properties.mPItem.items.properties.orderable.properties.productIdentifiers.properties.productId.title` | string |  |
| `properties.mPItem.items.properties.orderable.properties.productIdentifiers.properties.productId.type` | string |  |
| `properties.mPItem.items.properties.orderable.properties.productIdentifiers.properties.productIdType.comments` | string |  |
| `properties.mPItem.items.properties.orderable.properties.productIdentifiers.properties.productIdType.description` | string |  |
| `properties.mPItem.items.properties.orderable.properties.productIdentifiers.properties.productIdType.enum[]` | string |  |
| `properties.mPItem.items.properties.orderable.properties.productIdentifiers.properties.productIdType.examples` | string |  |
| `properties.mPItem.items.properties.orderable.properties.productIdentifiers.properties.productIdType.title` | string |  |
| `properties.mPItem.items.properties.orderable.properties.productIdentifiers.properties.productIdType.type` | string |  |
| `properties.mPItem.items.properties.orderable.properties.productIdentifiers.required[]` | string |  |
| `properties.mPItem.items.properties.orderable.properties.productIdentifiers.title` | string |  |
| `properties.mPItem.items.properties.orderable.properties.productIdentifiers.type` | string |  |
| `properties.mPItem.items.properties.orderable.properties.requiredStorageCondition.$schema` | string |  |
| `properties.mPItem.items.properties.orderable.properties.requiredStorageCondition.comments` | string |  |
| `properties.mPItem.items.properties.orderable.properties.requiredStorageCondition.description` | string |  |
| `properties.mPItem.items.properties.orderable.properties.requiredStorageCondition.examples` | string |  |
| `properties.mPItem.items.properties.orderable.properties.requiredStorageCondition.items.enum[]` | string |  |
| `properties.mPItem.items.properties.orderable.properties.requiredStorageCondition.items.type` | string |  |
| `properties.mPItem.items.properties.orderable.properties.requiredStorageCondition.minItems` | number |  |
| `properties.mPItem.items.properties.orderable.properties.requiredStorageCondition.title` | string |  |
| `properties.mPItem.items.properties.orderable.properties.requiredStorageCondition.type` | string |  |
| `properties.mPItem.items.properties.orderable.properties.safetyDataSheet.$schema` | string |  |
| `properties.mPItem.items.properties.orderable.properties.safetyDataSheet.comments` | string |  |
| `properties.mPItem.items.properties.orderable.properties.safetyDataSheet.description` | string |  |
| `properties.mPItem.items.properties.orderable.properties.safetyDataSheet.examples` | string |  |
| `properties.mPItem.items.properties.orderable.properties.safetyDataSheet.items.format` | string |  |
| `properties.mPItem.items.properties.orderable.properties.safetyDataSheet.items.maxLength` | number |  |
| `properties.mPItem.items.properties.orderable.properties.safetyDataSheet.items.type` | string |  |
| `properties.mPItem.items.properties.orderable.properties.safetyDataSheet.minItems` | number |  |
| `properties.mPItem.items.properties.orderable.properties.safetyDataSheet.title` | string |  |
| `properties.mPItem.items.properties.orderable.properties.safetyDataSheet.type` | string |  |
| `properties.mPItem.items.properties.orderable.properties.shipsInOriginalPackaging.comments` | string |  |
| `properties.mPItem.items.properties.orderable.properties.shipsInOriginalPackaging.description` | string |  |
| `properties.mPItem.items.properties.orderable.properties.shipsInOriginalPackaging.enum[]` | string |  |
| `properties.mPItem.items.properties.orderable.properties.shipsInOriginalPackaging.examples` | string |  |
| `properties.mPItem.items.properties.orderable.properties.shipsInOriginalPackaging.title` | string |  |
| `properties.mPItem.items.properties.orderable.properties.shipsInOriginalPackaging.type` | string |  |
| `properties.mPItem.items.properties.orderable.properties.sku.comments` | string |  |
| `properties.mPItem.items.properties.orderable.properties.sku.description` | string |  |
| `properties.mPItem.items.properties.orderable.properties.sku.examples[]` | string |  |
| `properties.mPItem.items.properties.orderable.properties.sku.maxLength` | number |  |
| `properties.mPItem.items.properties.orderable.properties.sku.minLength` | number |  |
| `properties.mPItem.items.properties.orderable.properties.sku.title` | string |  |
| `properties.mPItem.items.properties.orderable.properties.sku.type` | string |  |
| `properties.mPItem.items.properties.orderable.properties.skuUpdate.comments` | string |  |
| `properties.mPItem.items.properties.orderable.properties.skuUpdate.description` | string |  |
| `properties.mPItem.items.properties.orderable.properties.skuUpdate.enum[]` | string |  |
| `properties.mPItem.items.properties.orderable.properties.skuUpdate.examples` | string |  |
| `properties.mPItem.items.properties.orderable.properties.skuUpdate.title` | string |  |
| `properties.mPItem.items.properties.orderable.properties.skuUpdate.type` | string |  |
| `properties.mPItem.items.properties.orderable.properties.startDate.comments` | string |  |
| `properties.mPItem.items.properties.orderable.properties.startDate.description` | string |  |
| `properties.mPItem.items.properties.orderable.properties.startDate.examples[]` | string |  |
| `properties.mPItem.items.properties.orderable.properties.startDate.format` | string |  |
| `properties.mPItem.items.properties.orderable.properties.startDate.title` | string |  |
| `properties.mPItem.items.properties.orderable.properties.startDate.type` | string |  |
| `properties.mPItem.items.properties.orderable.properties.stateRestrictions.$schema` | string |  |
| `properties.mPItem.items.properties.orderable.properties.stateRestrictions.comments` | string |  |
| `properties.mPItem.items.properties.orderable.properties.stateRestrictions.description` | string |  |
| `properties.mPItem.items.properties.orderable.properties.stateRestrictions.examples` | string |  |
| `properties.mPItem.items.properties.orderable.properties.stateRestrictions.items.$schema` | string |  |
| `properties.mPItem.items.properties.orderable.properties.stateRestrictions.items.additionalProperties` | boolean |  |
| `properties.mPItem.items.properties.orderable.properties.stateRestrictions.items.properties.stateRestrictionsText.comments` | string |  |
| `properties.mPItem.items.properties.orderable.properties.stateRestrictions.items.properties.stateRestrictionsText.description` | string |  |
| `properties.mPItem.items.properties.orderable.properties.stateRestrictions.items.properties.stateRestrictionsText.enum[]` | string |  |
| `properties.mPItem.items.properties.orderable.properties.stateRestrictions.items.properties.stateRestrictionsText.examples` | string |  |
| `properties.mPItem.items.properties.orderable.properties.stateRestrictions.items.properties.stateRestrictionsText.title` | string |  |
| `properties.mPItem.items.properties.orderable.properties.stateRestrictions.items.properties.stateRestrictionsText.type` | string |  |
| `properties.mPItem.items.properties.orderable.properties.stateRestrictions.items.properties.states.comments` | string |  |
| `properties.mPItem.items.properties.orderable.properties.stateRestrictions.items.properties.states.description` | string |  |
| `properties.mPItem.items.properties.orderable.properties.stateRestrictions.items.properties.states.enum[]` | string |  |
| `properties.mPItem.items.properties.orderable.properties.stateRestrictions.items.properties.states.examples` | string |  |
| `properties.mPItem.items.properties.orderable.properties.stateRestrictions.items.properties.states.title` | string |  |
| `properties.mPItem.items.properties.orderable.properties.stateRestrictions.items.properties.states.type` | string |  |
| `properties.mPItem.items.properties.orderable.properties.stateRestrictions.items.properties.zipCodes.comments` | string |  |
| `properties.mPItem.items.properties.orderable.properties.stateRestrictions.items.properties.zipCodes.description` | string |  |
| `properties.mPItem.items.properties.orderable.properties.stateRestrictions.items.properties.zipCodes.examples[]` | string |  |
| `properties.mPItem.items.properties.orderable.properties.stateRestrictions.items.properties.zipCodes.maxLength` | number |  |
| `properties.mPItem.items.properties.orderable.properties.stateRestrictions.items.properties.zipCodes.minLength` | number |  |
| `properties.mPItem.items.properties.orderable.properties.stateRestrictions.items.properties.zipCodes.title` | string |  |
| `properties.mPItem.items.properties.orderable.properties.stateRestrictions.items.properties.zipCodes.type` | string |  |
| `properties.mPItem.items.properties.orderable.properties.stateRestrictions.items.required[]` | string |  |
| `properties.mPItem.items.properties.orderable.properties.stateRestrictions.items.type` | string |  |
| `properties.mPItem.items.properties.orderable.properties.stateRestrictions.minItems` | number |  |
| `properties.mPItem.items.properties.orderable.properties.stateRestrictions.title` | string |  |
| `properties.mPItem.items.properties.orderable.properties.stateRestrictions.type` | string |  |
| `properties.mPItem.items.properties.orderable.properties.thirdPartyProductFulfillmentType.$schema` | string |  |
| `properties.mPItem.items.properties.orderable.properties.thirdPartyProductFulfillmentType.comments` | string |  |
| `properties.mPItem.items.properties.orderable.properties.thirdPartyProductFulfillmentType.description` | string |  |
| `properties.mPItem.items.properties.orderable.properties.thirdPartyProductFulfillmentType.examples` | string |  |
| `properties.mPItem.items.properties.orderable.properties.thirdPartyProductFulfillmentType.items.enum[]` | string |  |
| `properties.mPItem.items.properties.orderable.properties.thirdPartyProductFulfillmentType.items.type` | string |  |
| `properties.mPItem.items.properties.orderable.properties.thirdPartyProductFulfillmentType.minItems` | number |  |
| `properties.mPItem.items.properties.orderable.properties.thirdPartyProductFulfillmentType.title` | string |  |
| `properties.mPItem.items.properties.orderable.properties.thirdPartyProductFulfillmentType.type` | string |  |
| `properties.mPItem.items.properties.orderable.required[]` | string |  |
| `properties.mPItem.items.properties.orderable.type` | string |  |
| `properties.mPItem.items.properties.tradeItem.$schema` | string |  |
| `properties.mPItem.items.properties.tradeItem.additionalProperties` | boolean |  |
| `properties.mPItem.items.properties.tradeItem.properties.case.$schema` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.case.additionalProperties` | boolean |  |
| `properties.mPItem.items.properties.tradeItem.properties.case.comments` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.case.description` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.case.examples` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.case.properties.caseDepth.comments` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.case.properties.caseDepth.description` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.case.properties.caseDepth.examples[]` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.case.properties.caseDepth.maximum` | number |  |
| `properties.mPItem.items.properties.tradeItem.properties.case.properties.caseDepth.minimum` | number |  |
| `properties.mPItem.items.properties.tradeItem.properties.case.properties.caseDepth.multipleOf` | number |  |
| `properties.mPItem.items.properties.tradeItem.properties.case.properties.caseDepth.title` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.case.properties.caseDepth.type` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.case.properties.caseGTIN.comments` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.case.properties.caseGTIN.description` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.case.properties.caseGTIN.examples[]` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.case.properties.caseGTIN.maxLength` | number |  |
| `properties.mPItem.items.properties.tradeItem.properties.case.properties.caseGTIN.minLength` | number |  |
| `properties.mPItem.items.properties.tradeItem.properties.case.properties.caseGTIN.title` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.case.properties.caseGTIN.type` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.case.properties.caseHeight.comments` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.case.properties.caseHeight.description` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.case.properties.caseHeight.examples[]` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.case.properties.caseHeight.maximum` | number |  |
| `properties.mPItem.items.properties.tradeItem.properties.case.properties.caseHeight.minimum` | number |  |
| `properties.mPItem.items.properties.tradeItem.properties.case.properties.caseHeight.multipleOf` | number |  |
| `properties.mPItem.items.properties.tradeItem.properties.case.properties.caseHeight.title` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.case.properties.caseHeight.type` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.case.properties.caseWeight.comments` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.case.properties.caseWeight.description` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.case.properties.caseWeight.examples[]` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.case.properties.caseWeight.maximum` | number |  |
| `properties.mPItem.items.properties.tradeItem.properties.case.properties.caseWeight.minimum` | number |  |
| `properties.mPItem.items.properties.tradeItem.properties.case.properties.caseWeight.multipleOf` | number |  |
| `properties.mPItem.items.properties.tradeItem.properties.case.properties.caseWeight.title` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.case.properties.caseWeight.type` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.case.properties.caseWidth.comments` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.case.properties.caseWidth.description` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.case.properties.caseWidth.examples[]` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.case.properties.caseWidth.maximum` | number |  |
| `properties.mPItem.items.properties.tradeItem.properties.case.properties.caseWidth.minimum` | number |  |
| `properties.mPItem.items.properties.tradeItem.properties.case.properties.caseWidth.multipleOf` | number |  |
| `properties.mPItem.items.properties.tradeItem.properties.case.properties.caseWidth.title` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.case.properties.caseWidth.type` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.case.properties.qtySellableItemsCase.comments` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.case.properties.qtySellableItemsCase.description` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.case.properties.qtySellableItemsCase.examples[]` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.case.properties.qtySellableItemsCase.maximum` | number |  |
| `properties.mPItem.items.properties.tradeItem.properties.case.properties.qtySellableItemsCase.minimum` | number |  |
| `properties.mPItem.items.properties.tradeItem.properties.case.properties.qtySellableItemsCase.title` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.case.properties.qtySellableItemsCase.type` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.case.required[]` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.case.title` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.case.type` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.countryOfOriginAssembly.$schema` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.countryOfOriginAssembly.comments` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.countryOfOriginAssembly.description` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.countryOfOriginAssembly.examples` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.countryOfOriginAssembly.items.enum[]` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.countryOfOriginAssembly.items.type` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.countryOfOriginAssembly.minItems` | number |  |
| `properties.mPItem.items.properties.tradeItem.properties.countryOfOriginAssembly.title` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.countryOfOriginAssembly.type` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.each.$schema` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.each.additionalProperties` | boolean |  |
| `properties.mPItem.items.properties.tradeItem.properties.each.comments` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.each.description` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.each.examples` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.each.properties.eachDepth.comments` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.each.properties.eachDepth.description` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.each.properties.eachDepth.examples[]` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.each.properties.eachDepth.maximum` | number |  |
| `properties.mPItem.items.properties.tradeItem.properties.each.properties.eachDepth.minimum` | number |  |
| `properties.mPItem.items.properties.tradeItem.properties.each.properties.eachDepth.multipleOf` | number |  |
| `properties.mPItem.items.properties.tradeItem.properties.each.properties.eachDepth.title` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.each.properties.eachDepth.type` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.each.properties.eachGTIN.comments` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.each.properties.eachGTIN.description` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.each.properties.eachGTIN.examples[]` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.each.properties.eachGTIN.maxLength` | number |  |
| `properties.mPItem.items.properties.tradeItem.properties.each.properties.eachGTIN.minLength` | number |  |
| `properties.mPItem.items.properties.tradeItem.properties.each.properties.eachGTIN.title` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.each.properties.eachGTIN.type` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.each.properties.eachHeight.comments` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.each.properties.eachHeight.description` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.each.properties.eachHeight.examples[]` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.each.properties.eachHeight.maximum` | number |  |
| `properties.mPItem.items.properties.tradeItem.properties.each.properties.eachHeight.minimum` | number |  |
| `properties.mPItem.items.properties.tradeItem.properties.each.properties.eachHeight.multipleOf` | number |  |
| `properties.mPItem.items.properties.tradeItem.properties.each.properties.eachHeight.title` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.each.properties.eachHeight.type` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.each.properties.eachWeight.comments` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.each.properties.eachWeight.description` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.each.properties.eachWeight.examples[]` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.each.properties.eachWeight.maximum` | number |  |
| `properties.mPItem.items.properties.tradeItem.properties.each.properties.eachWeight.minimum` | number |  |
| `properties.mPItem.items.properties.tradeItem.properties.each.properties.eachWeight.multipleOf` | number |  |
| `properties.mPItem.items.properties.tradeItem.properties.each.properties.eachWeight.title` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.each.properties.eachWeight.type` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.each.properties.eachWidth.comments` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.each.properties.eachWidth.description` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.each.properties.eachWidth.examples[]` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.each.properties.eachWidth.maximum` | number |  |
| `properties.mPItem.items.properties.tradeItem.properties.each.properties.eachWidth.minimum` | number |  |
| `properties.mPItem.items.properties.tradeItem.properties.each.properties.eachWidth.multipleOf` | number |  |
| `properties.mPItem.items.properties.tradeItem.properties.each.properties.eachWidth.title` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.each.properties.eachWidth.type` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.each.required[]` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.each.title` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.each.type` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.innerPack.$schema` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.innerPack.additionalProperties` | boolean |  |
| `properties.mPItem.items.properties.tradeItem.properties.innerPack.comments` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.innerPack.description` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.innerPack.examples` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.innerPack.properties.innerPackDepth.comments` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.innerPack.properties.innerPackDepth.description` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.innerPack.properties.innerPackDepth.examples[]` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.innerPack.properties.innerPackDepth.maximum` | number |  |
| `properties.mPItem.items.properties.tradeItem.properties.innerPack.properties.innerPackDepth.minimum` | number |  |
| `properties.mPItem.items.properties.tradeItem.properties.innerPack.properties.innerPackDepth.multipleOf` | number |  |
| `properties.mPItem.items.properties.tradeItem.properties.innerPack.properties.innerPackDepth.title` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.innerPack.properties.innerPackDepth.type` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.innerPack.properties.innerPackGTIN.comments` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.innerPack.properties.innerPackGTIN.description` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.innerPack.properties.innerPackGTIN.examples[]` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.innerPack.properties.innerPackGTIN.maxLength` | number |  |
| `properties.mPItem.items.properties.tradeItem.properties.innerPack.properties.innerPackGTIN.minLength` | number |  |
| `properties.mPItem.items.properties.tradeItem.properties.innerPack.properties.innerPackGTIN.title` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.innerPack.properties.innerPackGTIN.type` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.innerPack.properties.innerPackHeight.comments` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.innerPack.properties.innerPackHeight.description` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.innerPack.properties.innerPackHeight.examples[]` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.innerPack.properties.innerPackHeight.maximum` | number |  |
| `properties.mPItem.items.properties.tradeItem.properties.innerPack.properties.innerPackHeight.minimum` | number |  |
| `properties.mPItem.items.properties.tradeItem.properties.innerPack.properties.innerPackHeight.multipleOf` | number |  |
| `properties.mPItem.items.properties.tradeItem.properties.innerPack.properties.innerPackHeight.title` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.innerPack.properties.innerPackHeight.type` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.innerPack.properties.innerPackWeight.comments` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.innerPack.properties.innerPackWeight.description` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.innerPack.properties.innerPackWeight.examples[]` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.innerPack.properties.innerPackWeight.maximum` | number |  |
| `properties.mPItem.items.properties.tradeItem.properties.innerPack.properties.innerPackWeight.minimum` | number |  |
| `properties.mPItem.items.properties.tradeItem.properties.innerPack.properties.innerPackWeight.multipleOf` | number |  |
| `properties.mPItem.items.properties.tradeItem.properties.innerPack.properties.innerPackWeight.title` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.innerPack.properties.innerPackWeight.type` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.innerPack.properties.innerPackWidth.comments` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.innerPack.properties.innerPackWidth.description` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.innerPack.properties.innerPackWidth.examples[]` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.innerPack.properties.innerPackWidth.maximum` | number |  |
| `properties.mPItem.items.properties.tradeItem.properties.innerPack.properties.innerPackWidth.minimum` | number |  |
| `properties.mPItem.items.properties.tradeItem.properties.innerPack.properties.innerPackWidth.multipleOf` | number |  |
| `properties.mPItem.items.properties.tradeItem.properties.innerPack.properties.innerPackWidth.title` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.innerPack.properties.innerPackWidth.type` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.innerPack.properties.qtySellableItemsInnerPack.comments` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.innerPack.properties.qtySellableItemsInnerPack.description` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.innerPack.properties.qtySellableItemsInnerPack.examples[]` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.innerPack.properties.qtySellableItemsInnerPack.maximum` | number |  |
| `properties.mPItem.items.properties.tradeItem.properties.innerPack.properties.qtySellableItemsInnerPack.minimum` | number |  |
| `properties.mPItem.items.properties.tradeItem.properties.innerPack.properties.qtySellableItemsInnerPack.title` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.innerPack.properties.qtySellableItemsInnerPack.type` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.innerPack.required[]` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.innerPack.title` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.innerPack.type` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.orderableGTIN.comments` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.orderableGTIN.description` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.orderableGTIN.examples[]` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.orderableGTIN.maxLength` | number |  |
| `properties.mPItem.items.properties.tradeItem.properties.orderableGTIN.minLength` | number |  |
| `properties.mPItem.items.properties.tradeItem.properties.orderableGTIN.title` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.orderableGTIN.type` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.pallet.$schema` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.pallet.additionalProperties` | boolean |  |
| `properties.mPItem.items.properties.tradeItem.properties.pallet.comments` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.pallet.description` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.pallet.examples` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.pallet.properties.palletDepth.comments` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.pallet.properties.palletDepth.description` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.pallet.properties.palletDepth.examples[]` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.pallet.properties.palletDepth.maximum` | number |  |
| `properties.mPItem.items.properties.tradeItem.properties.pallet.properties.palletDepth.minimum` | number |  |
| `properties.mPItem.items.properties.tradeItem.properties.pallet.properties.palletDepth.multipleOf` | number |  |
| `properties.mPItem.items.properties.tradeItem.properties.pallet.properties.palletDepth.title` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.pallet.properties.palletDepth.type` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.pallet.properties.palletGTIN.comments` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.pallet.properties.palletGTIN.description` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.pallet.properties.palletGTIN.examples[]` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.pallet.properties.palletGTIN.maxLength` | number |  |
| `properties.mPItem.items.properties.tradeItem.properties.pallet.properties.palletGTIN.minLength` | number |  |
| `properties.mPItem.items.properties.tradeItem.properties.pallet.properties.palletGTIN.title` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.pallet.properties.palletGTIN.type` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.pallet.properties.palletHeight.comments` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.pallet.properties.palletHeight.description` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.pallet.properties.palletHeight.examples[]` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.pallet.properties.palletHeight.maximum` | number |  |
| `properties.mPItem.items.properties.tradeItem.properties.pallet.properties.palletHeight.minimum` | number |  |
| `properties.mPItem.items.properties.tradeItem.properties.pallet.properties.palletHeight.multipleOf` | number |  |
| `properties.mPItem.items.properties.tradeItem.properties.pallet.properties.palletHeight.title` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.pallet.properties.palletHeight.type` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.pallet.properties.palletWeight.comments` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.pallet.properties.palletWeight.description` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.pallet.properties.palletWeight.examples[]` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.pallet.properties.palletWeight.maximum` | number |  |
| `properties.mPItem.items.properties.tradeItem.properties.pallet.properties.palletWeight.minimum` | number |  |
| `properties.mPItem.items.properties.tradeItem.properties.pallet.properties.palletWeight.multipleOf` | number |  |
| `properties.mPItem.items.properties.tradeItem.properties.pallet.properties.palletWeight.title` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.pallet.properties.palletWeight.type` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.pallet.properties.palletWidth.comments` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.pallet.properties.palletWidth.description` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.pallet.properties.palletWidth.examples[]` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.pallet.properties.palletWidth.maximum` | number |  |
| `properties.mPItem.items.properties.tradeItem.properties.pallet.properties.palletWidth.minimum` | number |  |
| `properties.mPItem.items.properties.tradeItem.properties.pallet.properties.palletWidth.multipleOf` | number |  |
| `properties.mPItem.items.properties.tradeItem.properties.pallet.properties.palletWidth.title` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.pallet.properties.palletWidth.type` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.pallet.properties.qtySellableItemsPallet.comments` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.pallet.properties.qtySellableItemsPallet.description` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.pallet.properties.qtySellableItemsPallet.examples[]` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.pallet.properties.qtySellableItemsPallet.maximum` | number |  |
| `properties.mPItem.items.properties.tradeItem.properties.pallet.properties.qtySellableItemsPallet.minimum` | number |  |
| `properties.mPItem.items.properties.tradeItem.properties.pallet.properties.qtySellableItemsPallet.title` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.pallet.properties.qtySellableItemsPallet.type` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.pallet.required[]` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.pallet.title` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.pallet.type` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.sku.comments` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.sku.description` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.sku.examples[]` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.sku.maxLength` | number |  |
| `properties.mPItem.items.properties.tradeItem.properties.sku.minLength` | number |  |
| `properties.mPItem.items.properties.tradeItem.properties.sku.title` | string |  |
| `properties.mPItem.items.properties.tradeItem.properties.sku.type` | string |  |
| `properties.mPItem.items.properties.tradeItem.required[]` | string |  |
| `properties.mPItem.items.properties.tradeItem.type` | string |  |
| `properties.mPItem.items.properties.visible.$schema` | string |  |
| `properties.mPItem.items.properties.visible.additionalProperties` | boolean |  |
| `properties.mPItem.items.properties.visible.oneOf[].$schema` | string |  |
| `properties.mPItem.items.properties.visible.oneOf[].required[]` | string |  |
| `properties.mPItem.items.properties.visible.oneOf[].type` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.$schema` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.additionalProperties` | boolean |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.allOf[].if.properties.hasWrittenWarranty.enum[]` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.allOf[].if.properties.hasWrittenWarranty.type` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.allOf[].if.required[]` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.allOf[].then.required[]` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.assembledProductHeight.$schema` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.assembledProductHeight.additionalProperties` | boolean |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.assembledProductHeight.comments` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.assembledProductHeight.description` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.assembledProductHeight.examples[]` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.assembledProductHeight.properties.measure.comments` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.assembledProductHeight.properties.measure.description` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.assembledProductHeight.properties.measure.examples[]` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.assembledProductHeight.properties.measure.maximum` | number |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.assembledProductHeight.properties.measure.minimum` | number |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.assembledProductHeight.properties.measure.multipleOf` | number |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.assembledProductHeight.properties.measure.title` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.assembledProductHeight.properties.measure.type` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.assembledProductHeight.properties.unit.comments` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.assembledProductHeight.properties.unit.description` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.assembledProductHeight.properties.unit.enum[]` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.assembledProductHeight.properties.unit.examples[]` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.assembledProductHeight.properties.unit.title` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.assembledProductHeight.properties.unit.type` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.assembledProductHeight.required[]` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.assembledProductHeight.title` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.assembledProductHeight.type` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.assembledProductLength.$schema` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.assembledProductLength.additionalProperties` | boolean |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.assembledProductLength.comments` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.assembledProductLength.description` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.assembledProductLength.examples[]` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.assembledProductLength.properties.measure.comments` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.assembledProductLength.properties.measure.description` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.assembledProductLength.properties.measure.examples[]` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.assembledProductLength.properties.measure.maximum` | number |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.assembledProductLength.properties.measure.minimum` | number |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.assembledProductLength.properties.measure.multipleOf` | number |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.assembledProductLength.properties.measure.title` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.assembledProductLength.properties.measure.type` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.assembledProductLength.properties.unit.comments` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.assembledProductLength.properties.unit.description` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.assembledProductLength.properties.unit.enum[]` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.assembledProductLength.properties.unit.examples[]` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.assembledProductLength.properties.unit.title` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.assembledProductLength.properties.unit.type` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.assembledProductLength.required[]` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.assembledProductLength.title` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.assembledProductLength.type` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.assembledProductWeight.$schema` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.assembledProductWeight.additionalProperties` | boolean |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.assembledProductWeight.comments` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.assembledProductWeight.description` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.assembledProductWeight.examples[]` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.assembledProductWeight.properties.measure.comments` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.assembledProductWeight.properties.measure.description` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.assembledProductWeight.properties.measure.examples[]` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.assembledProductWeight.properties.measure.maximum` | number |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.assembledProductWeight.properties.measure.minimum` | number |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.assembledProductWeight.properties.measure.multipleOf` | number |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.assembledProductWeight.properties.measure.title` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.assembledProductWeight.properties.measure.type` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.assembledProductWeight.properties.unit.comments` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.assembledProductWeight.properties.unit.description` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.assembledProductWeight.properties.unit.enum[]` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.assembledProductWeight.properties.unit.examples[]` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.assembledProductWeight.properties.unit.title` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.assembledProductWeight.properties.unit.type` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.assembledProductWeight.required[]` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.assembledProductWeight.title` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.assembledProductWeight.type` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.assembledProductWidth.$schema` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.assembledProductWidth.additionalProperties` | boolean |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.assembledProductWidth.comments` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.assembledProductWidth.description` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.assembledProductWidth.examples[]` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.assembledProductWidth.properties.measure.comments` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.assembledProductWidth.properties.measure.description` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.assembledProductWidth.properties.measure.examples[]` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.assembledProductWidth.properties.measure.maximum` | number |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.assembledProductWidth.properties.measure.minimum` | number |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.assembledProductWidth.properties.measure.multipleOf` | number |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.assembledProductWidth.properties.measure.title` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.assembledProductWidth.properties.measure.type` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.assembledProductWidth.properties.unit.comments` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.assembledProductWidth.properties.unit.description` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.assembledProductWidth.properties.unit.enum[]` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.assembledProductWidth.properties.unit.examples[]` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.assembledProductWidth.properties.unit.title` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.assembledProductWidth.properties.unit.type` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.assembledProductWidth.required[]` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.assembledProductWidth.title` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.assembledProductWidth.type` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.brand.comments` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.brand.description` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.brand.examples[]` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.brand.maxLength` | number |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.brand.minLength` | number |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.brand.title` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.brand.type` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.character.$schema` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.character.comments` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.character.description` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.character.examples[]` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.character.items.maxLength` | number |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.character.items.minLength` | number |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.character.items.type` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.character.minItems` | number |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.character.title` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.character.type` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.characterGroup.$schema` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.characterGroup.comments` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.characterGroup.description` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.characterGroup.examples[]` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.characterGroup.items.maxLength` | number |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.characterGroup.items.minLength` | number |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.characterGroup.items.type` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.characterGroup.minItems` | number |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.characterGroup.title` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.characterGroup.type` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.collection.comments` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.collection.description` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.collection.examples[]` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.collection.maxLength` | number |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.collection.minLength` | number |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.collection.title` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.collection.type` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.color.comments` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.color.description` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.color.examples[]` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.color.maxLength` | number |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.color.minLength` | number |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.color.title` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.color.type` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.colorCategory.$schema` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.colorCategory.comments` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.colorCategory.description` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.colorCategory.examples` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.colorCategory.items.enum[]` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.colorCategory.items.type` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.colorCategory.minItems` | number |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.colorCategory.title` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.colorCategory.type` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.condition.comments` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.condition.description` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.condition.enum[]` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.condition.examples` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.condition.title` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.condition.type` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.count.comments` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.count.description` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.count.examples[]` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.count.maximum` | number |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.count.minimum` | number |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.count.title` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.count.type` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.countPerPack.comments` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.countPerPack.description` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.countPerPack.examples[]` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.countPerPack.maximum` | number |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.countPerPack.minimum` | number |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.countPerPack.title` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.countPerPack.type` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.fabricCareInstructions.$schema` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.fabricCareInstructions.comments` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.fabricCareInstructions.description` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.fabricCareInstructions.examples[]` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.fabricCareInstructions.items.maxLength` | number |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.fabricCareInstructions.items.minLength` | number |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.fabricCareInstructions.items.type` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.fabricCareInstructions.minItems` | number |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.fabricCareInstructions.title` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.fabricCareInstructions.type` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.fabricContent.$schema` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.fabricContent.comments` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.fabricContent.description` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.fabricContent.examples[]` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.fabricContent.items.$schema` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.fabricContent.items.additionalProperties` | boolean |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.fabricContent.items.properties.materialName.comments` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.fabricContent.items.properties.materialName.description` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.fabricContent.items.properties.materialName.examples[]` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.fabricContent.items.properties.materialName.maxLength` | number |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.fabricContent.items.properties.materialName.minLength` | number |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.fabricContent.items.properties.materialName.title` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.fabricContent.items.properties.materialName.type` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.fabricContent.items.properties.materialPercentage.comments` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.fabricContent.items.properties.materialPercentage.description` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.fabricContent.items.properties.materialPercentage.examples[]` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.fabricContent.items.properties.materialPercentage.maximum` | number |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.fabricContent.items.properties.materialPercentage.minimum` | number |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.fabricContent.items.properties.materialPercentage.multipleOf` | number |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.fabricContent.items.properties.materialPercentage.title` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.fabricContent.items.properties.materialPercentage.type` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.fabricContent.items.required[]` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.fabricContent.items.type` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.fabricContent.minItems` | number |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.fabricContent.title` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.fabricContent.type` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.features.$schema` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.features.comments` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.features.description` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.features.examples` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.features.items.enum[]` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.features.items.type` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.features.minItems` | number |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.features.title` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.features.type` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.frameColorConfiguration.$schema` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.frameColorConfiguration.comments` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.frameColorConfiguration.description` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.frameColorConfiguration.examples[]` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.frameColorConfiguration.items.maxLength` | number |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.frameColorConfiguration.items.minLength` | number |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.frameColorConfiguration.items.type` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.frameColorConfiguration.minItems` | number |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.frameColorConfiguration.title` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.frameColorConfiguration.type` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.frontEndPhotoPartner.comments` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.frontEndPhotoPartner.description` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.frontEndPhotoPartner.enum[]` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.frontEndPhotoPartner.examples` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.frontEndPhotoPartner.title` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.frontEndPhotoPartner.type` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.gender.comments` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.gender.description` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.gender.enum[]` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.gender.examples` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.gender.title` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.gender.type` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.globalBrandLicense.$schema` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.globalBrandLicense.comments` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.globalBrandLicense.description` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.globalBrandLicense.examples[]` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.globalBrandLicense.items.maxLength` | number |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.globalBrandLicense.items.minLength` | number |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.globalBrandLicense.items.type` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.globalBrandLicense.minItems` | number |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.globalBrandLicense.title` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.globalBrandLicense.type` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.gramsPerSquareMeterGsm.$schema` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.gramsPerSquareMeterGsm.additionalProperties` | boolean |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.gramsPerSquareMeterGsm.comments` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.gramsPerSquareMeterGsm.description` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.gramsPerSquareMeterGsm.examples[]` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.gramsPerSquareMeterGsm.properties.measure.comments` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.gramsPerSquareMeterGsm.properties.measure.description` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.gramsPerSquareMeterGsm.properties.measure.examples[]` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.gramsPerSquareMeterGsm.properties.measure.maximum` | number |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.gramsPerSquareMeterGsm.properties.measure.minimum` | number |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.gramsPerSquareMeterGsm.properties.measure.title` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.gramsPerSquareMeterGsm.properties.measure.type` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.gramsPerSquareMeterGsm.properties.unit.comments` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.gramsPerSquareMeterGsm.properties.unit.description` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.gramsPerSquareMeterGsm.properties.unit.enum[]` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.gramsPerSquareMeterGsm.properties.unit.examples[]` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.gramsPerSquareMeterGsm.properties.unit.title` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.gramsPerSquareMeterGsm.properties.unit.type` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.gramsPerSquareMeterGsm.required[]` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.gramsPerSquareMeterGsm.title` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.gramsPerSquareMeterGsm.type` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.hasWrittenWarranty.comments` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.hasWrittenWarranty.description` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.hasWrittenWarranty.enum[]` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.hasWrittenWarranty.examples` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.hasWrittenWarranty.title` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.hasWrittenWarranty.type` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.homeDecorStyle.$schema` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.homeDecorStyle.comments` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.homeDecorStyle.description` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.homeDecorStyle.examples` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.homeDecorStyle.items.enum[]` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.homeDecorStyle.items.type` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.homeDecorStyle.minItems` | number |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.homeDecorStyle.title` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.homeDecorStyle.type` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.ibBlanketStyle.comments` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.ibBlanketStyle.description` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.ibBlanketStyle.enum[]` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.ibBlanketStyle.examples` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.ibBlanketStyle.title` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.ibBlanketStyle.type` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.isPrimaryVariant.comments` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.isPrimaryVariant.description` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.isPrimaryVariant.enum[]` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.isPrimaryVariant.examples` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.isPrimaryVariant.title` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.isPrimaryVariant.type` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.isProp65WarningRequired.comments` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.isProp65WarningRequired.description` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.isProp65WarningRequired.enum[]` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.isProp65WarningRequired.examples` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.isProp65WarningRequired.title` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.isProp65WarningRequired.type` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.keyFeatures.$schema` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.keyFeatures.comments` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.keyFeatures.description` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.keyFeatures.examples[]` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.keyFeatures.items.maxLength` | number |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.keyFeatures.items.minLength` | number |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.keyFeatures.items.type` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.keyFeatures.minItems` | number |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.keyFeatures.title` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.keyFeatures.type` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.lawLabelDisclosure.$schema` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.lawLabelDisclosure.additionalProperties` | boolean |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.lawLabelDisclosure.comments` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.lawLabelDisclosure.description` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.lawLabelDisclosure.examples` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.lawLabelDisclosure.properties.lawLabelIdentificationProvider.comments` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.lawLabelDisclosure.properties.lawLabelIdentificationProvider.description` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.lawLabelDisclosure.properties.lawLabelIdentificationProvider.enum[]` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.lawLabelDisclosure.properties.lawLabelIdentificationProvider.examples` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.lawLabelDisclosure.properties.lawLabelIdentificationProvider.title` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.lawLabelDisclosure.properties.lawLabelIdentificationProvider.type` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.lawLabelDisclosure.properties.lawLabelRegistrationNumber.comments` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.lawLabelDisclosure.properties.lawLabelRegistrationNumber.description` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.lawLabelDisclosure.properties.lawLabelRegistrationNumber.examples` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.lawLabelDisclosure.properties.lawLabelRegistrationNumber.maxLength` | number |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.lawLabelDisclosure.properties.lawLabelRegistrationNumber.minLength` | number |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.lawLabelDisclosure.properties.lawLabelRegistrationNumber.title` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.lawLabelDisclosure.properties.lawLabelRegistrationNumber.type` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.lawLabelDisclosure.required[]` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.lawLabelDisclosure.title` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.lawLabelDisclosure.type` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.mainImageUrl.comments` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.mainImageUrl.description` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.mainImageUrl.examples` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.mainImageUrl.format` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.mainImageUrl.maxLength` | number |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.mainImageUrl.minLength` | number |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.mainImageUrl.title` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.mainImageUrl.type` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.manufacturer.comments` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.manufacturer.description` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.manufacturer.examples[]` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.manufacturer.maxLength` | number |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.manufacturer.minLength` | number |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.manufacturer.title` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.manufacturer.type` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.manufacturerPartNumber.comments` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.manufacturerPartNumber.description` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.manufacturerPartNumber.examples[]` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.manufacturerPartNumber.maxLength` | number |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.manufacturerPartNumber.minLength` | number |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.manufacturerPartNumber.title` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.manufacturerPartNumber.type` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.maximumOrderQuantity.comments` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.maximumOrderQuantity.description` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.maximumOrderQuantity.examples[]` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.maximumOrderQuantity.maximum` | number |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.maximumOrderQuantity.minimum` | number |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.maximumOrderQuantity.title` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.maximumOrderQuantity.type` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.minimumOrderQuantity.comments` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.minimumOrderQuantity.description` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.minimumOrderQuantity.examples[]` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.minimumOrderQuantity.maximum` | number |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.minimumOrderQuantity.minimum` | number |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.minimumOrderQuantity.title` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.minimumOrderQuantity.type` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.modelNumber.comments` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.modelNumber.description` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.modelNumber.examples[]` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.modelNumber.maxLength` | number |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.modelNumber.minLength` | number |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.modelNumber.title` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.modelNumber.type` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.multipackQuantity.comments` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.multipackQuantity.description` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.multipackQuantity.examples[]` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.multipackQuantity.maximum` | number |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.multipackQuantity.minimum` | number |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.multipackQuantity.title` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.multipackQuantity.type` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.netContent.$schema` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.netContent.additionalProperties` | boolean |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.netContent.comments` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.netContent.description` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.netContent.examples` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.netContent.properties.productNetContentMeasure.comments` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.netContent.properties.productNetContentMeasure.description` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.netContent.properties.productNetContentMeasure.examples[]` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.netContent.properties.productNetContentMeasure.maximum` | number |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.netContent.properties.productNetContentMeasure.minimum` | number |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.netContent.properties.productNetContentMeasure.multipleOf` | number |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.netContent.properties.productNetContentMeasure.title` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.netContent.properties.productNetContentMeasure.type` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.netContent.properties.productNetContentUnit.comments` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.netContent.properties.productNetContentUnit.description` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.netContent.properties.productNetContentUnit.enum[]` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.netContent.properties.productNetContentUnit.examples` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.netContent.properties.productNetContentUnit.title` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.netContent.properties.productNetContentUnit.type` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.netContent.required[]` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.netContent.title` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.netContent.type` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.netContentStatement.comments` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.netContentStatement.description` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.netContentStatement.examples[]` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.netContentStatement.maxLength` | number |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.netContentStatement.minLength` | number |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.netContentStatement.title` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.netContentStatement.type` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.occasion.$schema` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.occasion.comments` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.occasion.description` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.occasion.examples[]` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.occasion.items.maxLength` | number |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.occasion.items.minLength` | number |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.occasion.items.type` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.occasion.minItems` | number |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.occasion.title` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.occasion.type` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.pattern.$schema` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.pattern.comments` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.pattern.description` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.pattern.examples[]` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.pattern.items.maxLength` | number |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.pattern.items.minLength` | number |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.pattern.items.type` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.pattern.minItems` | number |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.pattern.title` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.pattern.type` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.photoAccessoryItemSku.$schema` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.photoAccessoryItemSku.comments` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.photoAccessoryItemSku.description` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.photoAccessoryItemSku.examples[]` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.photoAccessoryItemSku.items.maxLength` | number |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.photoAccessoryItemSku.items.minLength` | number |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.photoAccessoryItemSku.items.type` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.photoAccessoryItemSku.minItems` | number |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.photoAccessoryItemSku.title` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.photoAccessoryItemSku.type` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.photoConfigurationAttributeNames.$schema` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.photoConfigurationAttributeNames.comments` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.photoConfigurationAttributeNames.description` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.photoConfigurationAttributeNames.examples` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.photoConfigurationAttributeNames.items.enum[]` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.photoConfigurationAttributeNames.items.type` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.photoConfigurationAttributeNames.minItems` | number |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.photoConfigurationAttributeNames.title` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.photoConfigurationAttributeNames.type` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.photoItemStoreUpc.comments` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.photoItemStoreUpc.description` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.photoItemStoreUpc.examples[]` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.photoItemStoreUpc.maxLength` | number |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.photoItemStoreUpc.minLength` | number |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.photoItemStoreUpc.title` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.photoItemStoreUpc.type` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.photoOrderQuantityTier.comments` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.photoOrderQuantityTier.description` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.photoOrderQuantityTier.examples[]` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.photoOrderQuantityTier.maximum` | number |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.photoOrderQuantityTier.minimum` | number |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.photoOrderQuantityTier.title` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.photoOrderQuantityTier.type` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.photoPaperFinishConfiguration.$schema` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.photoPaperFinishConfiguration.comments` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.photoPaperFinishConfiguration.description` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.photoPaperFinishConfiguration.examples` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.photoPaperFinishConfiguration.items.enum[]` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.photoPaperFinishConfiguration.items.type` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.photoPaperFinishConfiguration.minItems` | number |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.photoPaperFinishConfiguration.title` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.photoPaperFinishConfiguration.type` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.pieceCount.comments` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.pieceCount.description` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.pieceCount.examples[]` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.pieceCount.maximum` | number |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.pieceCount.minimum` | number |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.pieceCount.title` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.pieceCount.type` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.productLine.$schema` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.productLine.comments` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.productLine.description` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.productLine.examples[]` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.productLine.items.maxLength` | number |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.productLine.items.minLength` | number |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.productLine.items.type` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.productLine.minItems` | number |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.productLine.title` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.productLine.type` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.productName.comments` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.productName.description` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.productName.examples[]` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.productName.maxLength` | number |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.productName.minLength` | number |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.productName.title` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.productName.type` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.productSecondaryImageURL.$schema` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.productSecondaryImageURL.comments` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.productSecondaryImageURL.description` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.productSecondaryImageURL.examples` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.productSecondaryImageURL.items.format` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.productSecondaryImageURL.items.maxLength` | number |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.productSecondaryImageURL.items.minLength` | number |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.productSecondaryImageURL.items.type` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.productSecondaryImageURL.minItems` | number |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.productSecondaryImageURL.title` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.productSecondaryImageURL.type` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.prop65WarningText.comments` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.prop65WarningText.description` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.prop65WarningText.examples[]` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.prop65WarningText.maxLength` | number |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.prop65WarningText.minLength` | number |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.prop65WarningText.title` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.prop65WarningText.type` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.shortDescription.comments` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.shortDescription.description` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.shortDescription.examples[]` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.shortDescription.maxLength` | number |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.shortDescription.minLength` | number |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.shortDescription.title` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.shortDescription.type` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.size.comments` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.size.description` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.size.examples[]` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.size.maxLength` | number |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.size.minLength` | number |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.size.title` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.size.type` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.smallPartsWarnings.$schema` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.smallPartsWarnings.comments` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.smallPartsWarnings.description` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.smallPartsWarnings.examples` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.smallPartsWarnings.items.enum[]` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.smallPartsWarnings.items.type` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.smallPartsWarnings.minItems` | number |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.smallPartsWarnings.title` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.smallPartsWarnings.type` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.sportsLeague.$schema` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.sportsLeague.comments` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.sportsLeague.description` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.sportsLeague.examples[]` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.sportsLeague.items.maxLength` | number |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.sportsLeague.items.minLength` | number |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.sportsLeague.items.type` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.sportsLeague.minItems` | number |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.sportsLeague.title` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.sportsLeague.type` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.sportsTeam.$schema` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.sportsTeam.comments` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.sportsTeam.description` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.sportsTeam.examples[]` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.sportsTeam.items.maxLength` | number |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.sportsTeam.items.minLength` | number |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.sportsTeam.items.type` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.sportsTeam.minItems` | number |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.sportsTeam.title` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.sportsTeam.type` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.swatchImages.$schema` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.swatchImages.comments` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.swatchImages.description` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.swatchImages.examples` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.swatchImages.items.$schema` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.swatchImages.items.additionalProperties` | boolean |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.swatchImages.items.properties.swatchImageUrl.comments` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.swatchImages.items.properties.swatchImageUrl.description` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.swatchImages.items.properties.swatchImageUrl.examples[]` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.swatchImages.items.properties.swatchImageUrl.format` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.swatchImages.items.properties.swatchImageUrl.maxLength` | number |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.swatchImages.items.properties.swatchImageUrl.minLength` | number |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.swatchImages.items.properties.swatchImageUrl.title` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.swatchImages.items.properties.swatchImageUrl.type` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.swatchImages.items.properties.swatchVariantAttribute.comments` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.swatchImages.items.properties.swatchVariantAttribute.description` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.swatchImages.items.properties.swatchVariantAttribute.enum[]` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.swatchImages.items.properties.swatchVariantAttribute.examples` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.swatchImages.items.properties.swatchVariantAttribute.title` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.swatchImages.items.properties.swatchVariantAttribute.type` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.swatchImages.items.type` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.swatchImages.minItems` | number |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.swatchImages.title` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.swatchImages.type` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.theme.comments` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.theme.description` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.theme.examples[]` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.theme.maxLength` | number |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.theme.minLength` | number |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.theme.title` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.theme.type` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.thirdPartyAccreditationSymbolOnProductPackageCode.$schema` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.thirdPartyAccreditationSymbolOnProductPackageCode.comments` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.thirdPartyAccreditationSymbolOnProductPackageCode.description` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.thirdPartyAccreditationSymbolOnProductPackageCode.examples` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.thirdPartyAccreditationSymbolOnProductPackageCode.items.enum[]` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.thirdPartyAccreditationSymbolOnProductPackageCode.items.type` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.thirdPartyAccreditationSymbolOnProductPackageCode.minItems` | number |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.thirdPartyAccreditationSymbolOnProductPackageCode.title` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.thirdPartyAccreditationSymbolOnProductPackageCode.type` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.threadCount.comments` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.threadCount.description` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.threadCount.examples[]` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.threadCount.maximum` | number |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.threadCount.minimum` | number |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.threadCount.title` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.threadCount.type` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.variantAttributeNames.$schema` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.variantAttributeNames.comments` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.variantAttributeNames.description` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.variantAttributeNames.examples` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.variantAttributeNames.items.enum[]` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.variantAttributeNames.items.type` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.variantAttributeNames.minItems` | number |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.variantAttributeNames.title` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.variantAttributeNames.type` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.variantGroupId.comments` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.variantGroupId.description` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.variantGroupId.examples[]` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.variantGroupId.maxLength` | number |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.variantGroupId.minLength` | number |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.variantGroupId.title` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.variantGroupId.type` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.warrantyText.comments` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.warrantyText.description` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.warrantyText.examples[]` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.warrantyText.maxLength` | number |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.warrantyText.minLength` | number |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.warrantyText.title` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.warrantyText.type` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.warrantyURL.comments` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.warrantyURL.description` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.warrantyURL.examples[]` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.warrantyURL.format` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.warrantyURL.maxLength` | number |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.warrantyURL.minLength` | number |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.warrantyURL.title` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.warrantyURL.type` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.weavingTechnique.comments` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.weavingTechnique.description` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.weavingTechnique.examples[]` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.weavingTechnique.maxLength` | number |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.weavingTechnique.minLength` | number |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.weavingTechnique.title` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.properties.weavingTechnique.type` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.required[]` | string |  |
| `properties.mPItem.items.properties.visible.properties.babyBlankets.type` | string |  |
| `properties.mPItem.items.properties.visible.title` | string |  |
| `properties.mPItem.items.properties.visible.type` | string |  |
| `properties.mPItem.items.required[]` | string |  |
| `properties.mPItem.items.type` | string |  |
| `properties.mPItem.minItems` | number |  |
| `properties.mPItem.title` | string |  |
| `properties.mPItem.type` | string |  |
| `properties.mPItemFeedHeader.$schema` | string |  |
| `properties.mPItemFeedHeader.additionalProperties` | boolean |  |
| `properties.mPItemFeedHeader.properties.businessUnit.enum[]` | string |  |
| `properties.mPItemFeedHeader.properties.businessUnit.title` | string |  |
| `properties.mPItemFeedHeader.properties.businessUnit.type` | string |  |
| `properties.mPItemFeedHeader.properties.locale.enum[]` | string |  |
| `properties.mPItemFeedHeader.properties.locale.title` | string |  |
| `properties.mPItemFeedHeader.properties.locale.type` | string |  |
| `properties.mPItemFeedHeader.properties.version.enum[]` | string |  |
| `properties.mPItemFeedHeader.properties.version.title` | string |  |
| `properties.mPItemFeedHeader.properties.version.type` | string |  |
| `properties.mPItemFeedHeader.required[]` | string |  |
| `properties.mPItemFeedHeader.title` | string |  |
| `properties.mPItemFeedHeader.type` | string |  |
| `required[]` | string |  |
| `title` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Walmart API, this operation is `POST /v3/items/spec` (base URL `https://{{credentials.environment}}.walmartapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-spec.md) for the provider-specific parameters and requirements.

