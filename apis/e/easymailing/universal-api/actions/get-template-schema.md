# Easymailing: Get Template Schema

Retrieves the template schema from Easymailing.

```
GET https://connect.mindcloud.co/v1/universal/easymailing/latest/actions/get-template-schema
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Easymailing `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/easymailing/latest/actions/get-template-schema?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/easymailing/latest/actions/get-template-schema?${params}`, {
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
      "commonErrors": {
        "backgroundColor": "string",
        "content": "string",
        "fontColor": "string",
        "link": "https://example.com",
        "rowBackgroundColor": "string",
        "textAlign": "string",
        "url": "https://example.com"
      },
      "documentation": {
        "example": {
          "template": {
            "rows": [
              {
                "columns": [
                  {
                    "modules": [
                      {
                        "align": "string",
                        "color": "string",
                        "paddingBottom": 1,
                        "paddingLeft": 1,
                        "paddingRight": 1,
                        "paddingTop": 1,
                        "size": 1,
                        "text": "string",
                        "type": "string"
                      }
                    ],
                    "weight": 1
                  }
                ],
                "name": "Ava Chen"
              }
            ],
            "settings": {
              "backgroundColor": "string",
              "contentAreaBackgroundColor": "string",
              "width": 1
            },
            "type": "string"
          }
        },
        "moduleTypes": [
          "string"
        ],
        "rules": [
          "string"
        ]
      },
      "id": "string",
      "officialExample": {
        "template": {
          "metadata": {
            "description": "string",
            "lang": "string",
            "preheader": "string",
            "subject": "string",
            "title": "string"
          },
          "rows": [
            {
              "columns": [
                {
                  "weight": 1
                }
              ],
              "name": "Ava Chen"
            }
          ],
          "settings": {
            "backgroundColor": "string",
            "contentAreaBackgroundColor": "string",
            "linkColor": "https://example.com",
            "width": 1
          },
          "type": "string"
        }
      },
      "schema": {
        "additionalProperties": true,
        "definitions": {
          "borderRadius": {
            "maximum": 1,
            "minimum": 1,
            "type": "string"
          },
          "borderWidth": {
            "maximum": 1,
            "minimum": 1,
            "type": "string"
          },
          "padding": {
            "maximum": 1,
            "minimum": 1,
            "type": "string"
          },
          "typeOfModules": {
            "enum": [
              "string"
            ]
          }
        },
        "properties": {
          "template": {
            "additionalProperties": true,
            "properties": {
              "metadata": {
                "additionalProperties": true,
                "properties": {
                  "description": {
                    "type": "string"
                  },
                  "lang": {
                    "type": "string"
                  },
                  "preheader": {
                    "type": "string"
                  },
                  "subject": {
                    "type": "string"
                  },
                  "title": {
                    "type": "string"
                  }
                },
                "type": "string"
              },
              "rows": {
                "items": {
                  "additionalProperties": true,
                  "properties": {
                    "backgroundColor": {
                      "type": "string"
                    },
                    "backgroundImage": {
                      "type": "string"
                    },
                    "backgroundPosition": {
                      "type": "string"
                    },
                    "backgroundRepeat": {
                      "type": "string"
                    },
                    "borderColor": {
                      "type": "string"
                    },
                    "colStackOnMobile": {
                      "type": "string"
                    },
                    "columns": {
                      "items": {
                        "additionalProperties": true,
                        "properties": {
                          "backgroundColor": {
                            "type": "string"
                          },
                          "borderColor": {
                            "type": "string"
                          },
                          "customFields": {
                            "type": "string"
                          },
                          "modules": {
                            "items": {
                              "discriminator": {
                                "propertyName": "Ava Chen"
                              },
                              "oneOf": [
                                {
                                  "additionalProperties": true,
                                  "properties": {
                                    "align": {
                                      "enum": [
                                        "string"
                                      ]
                                    },
                                    "backgroundColor": {
                                      "type": "string"
                                    },
                                    "borderColor": {
                                      "type": "string"
                                    },
                                    "color": {
                                      "type": "string"
                                    },
                                    "customFields": {
                                      "type": "string"
                                    },
                                    "hoverBackgroundColor": {
                                      "type": "string"
                                    },
                                    "hoverBorderColor": {
                                      "type": "string"
                                    },
                                    "hoverColor": {
                                      "type": "string"
                                    },
                                    "href": {
                                      "type": "string"
                                    },
                                    "label": {
                                      "format": "string",
                                      "type": "string"
                                    },
                                    "locked": {
                                      "type": "string"
                                    },
                                    "size": {
                                      "minimum": 1,
                                      "type": "string"
                                    },
                                    "target": {
                                      "enum": [
                                        "string"
                                      ]
                                    },
                                    "text": {
                                      "format": "string",
                                      "type": "string"
                                    },
                                    "type": {
                                      "const": "string"
                                    }
                                  },
                                  "title": "string",
                                  "type": "string"
                                }
                              ],
                              "required": [
                                "string"
                              ],
                              "type": "string"
                            },
                            "type": "string"
                          },
                          "weight": {
                            "maximum": 1,
                            "minimum": 1,
                            "type": "string"
                          }
                        },
                        "required": [
                          "string"
                        ],
                        "title": "string",
                        "type": "string"
                      },
                      "maxItems": 1,
                      "minItems": 1,
                      "type": "string"
                    },
                    "columnsSpacing": {
                      "maximum": 1,
                      "minimum": 1,
                      "type": "string"
                    },
                    "contentAreaBackgroundColor": {
                      "type": "string"
                    },
                    "customFields": {
                      "type": "string"
                    },
                    "displayCondition": {
                      "properties": {
                        "after": {
                          "type": "string"
                        },
                        "before": {
                          "type": "string"
                        },
                        "description": {
                          "type": "string"
                        },
                        "label": {
                          "type": "string"
                        },
                        "type": {
                          "type": "string"
                        }
                      },
                      "required": [
                        "string"
                      ],
                      "type": "string"
                    },
                    "locked": {
                      "type": "string"
                    },
                    "metadata": {
                      "type": "string"
                    },
                    "name": {
                      "type": "Ava Chen"
                    },
                    "rowReverseColStackOnMobile": {
                      "type": "string"
                    },
                    "verticalAlign": {
                      "enum": [
                        "string"
                      ],
                      "type": "string"
                    }
                  },
                  "required": [
                    "string"
                  ],
                  "title": "string",
                  "type": "string"
                },
                "minItems": 1,
                "type": "string"
              },
              "settings": {
                "additionalProperties": true,
                "properties": {
                  "backgroundColor": {
                    "type": "string"
                  },
                  "contentAreaBackgroundColor": {
                    "type": "string"
                  },
                  "linkColor": {
                    "type": "https://example.com"
                  },
                  "width": {
                    "maximum": 1,
                    "minimum": 1,
                    "type": "string"
                  }
                },
                "type": "string"
              },
              "type": {
                "enum": [
                  "string"
                ],
                "type": "string"
              }
            },
            "required": [
              "string"
            ],
            "type": "string"
          }
        },
        "required": [
          "string"
        ],
        "title": "string",
        "type": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `commonErrors.backgroundColor` | string |  |
| `commonErrors.content` | string |  |
| `commonErrors.fontColor` | string |  |
| `commonErrors.link` | string |  |
| `commonErrors.rowBackgroundColor` | string |  |
| `commonErrors.textAlign` | string |  |
| `commonErrors.url` | string |  |
| `documentation.example.template.rows[].columns[].modules[].align` | string |  |
| `documentation.example.template.rows[].columns[].modules[].color` | string |  |
| `documentation.example.template.rows[].columns[].modules[].paddingBottom` | number |  |
| `documentation.example.template.rows[].columns[].modules[].paddingLeft` | number |  |
| `documentation.example.template.rows[].columns[].modules[].paddingRight` | number |  |
| `documentation.example.template.rows[].columns[].modules[].paddingTop` | number |  |
| `documentation.example.template.rows[].columns[].modules[].size` | number |  |
| `documentation.example.template.rows[].columns[].modules[].text` | string |  |
| `documentation.example.template.rows[].columns[].modules[].type` | string |  |
| `documentation.example.template.rows[].columns[].weight` | number |  |
| `documentation.example.template.rows[].name` | string |  |
| `documentation.example.template.settings.backgroundColor` | string |  |
| `documentation.example.template.settings.contentAreaBackgroundColor` | string |  |
| `documentation.example.template.settings.width` | number |  |
| `documentation.example.template.type` | string |  |
| `documentation.moduleTypes[]` | string |  |
| `documentation.rules[]` | string |  |
| `id` | string |  |
| `officialExample.template.metadata.description` | string |  |
| `officialExample.template.metadata.lang` | string |  |
| `officialExample.template.metadata.preheader` | string |  |
| `officialExample.template.metadata.subject` | string |  |
| `officialExample.template.metadata.title` | string |  |
| `officialExample.template.rows[].columns[].weight` | number |  |
| `officialExample.template.rows[].name` | string |  |
| `officialExample.template.settings.backgroundColor` | string |  |
| `officialExample.template.settings.contentAreaBackgroundColor` | string |  |
| `officialExample.template.settings.linkColor` | string |  |
| `officialExample.template.settings.width` | number |  |
| `officialExample.template.type` | string |  |
| `schema.additionalProperties` | boolean |  |
| `schema.definitions.borderRadius.maximum` | number |  |
| `schema.definitions.borderRadius.minimum` | number |  |
| `schema.definitions.borderRadius.type` | string |  |
| `schema.definitions.borderWidth.maximum` | number |  |
| `schema.definitions.borderWidth.minimum` | number |  |
| `schema.definitions.borderWidth.type` | string |  |
| `schema.definitions.padding.maximum` | number |  |
| `schema.definitions.padding.minimum` | number |  |
| `schema.definitions.padding.type` | string |  |
| `schema.definitions.typeOfModules.enum[]` | string |  |
| `schema.properties.template.additionalProperties` | boolean |  |
| `schema.properties.template.properties.metadata.additionalProperties` | boolean |  |
| `schema.properties.template.properties.metadata.properties.description.type` | string |  |
| `schema.properties.template.properties.metadata.properties.lang.type` | string |  |
| `schema.properties.template.properties.metadata.properties.preheader.type` | string |  |
| `schema.properties.template.properties.metadata.properties.subject.type` | string |  |
| `schema.properties.template.properties.metadata.properties.title.type` | string |  |
| `schema.properties.template.properties.metadata.type` | string |  |
| `schema.properties.template.properties.rows.items.additionalProperties` | boolean |  |
| `schema.properties.template.properties.rows.items.properties.backgroundColor.type` | string |  |
| `schema.properties.template.properties.rows.items.properties.backgroundImage.type` | string |  |
| `schema.properties.template.properties.rows.items.properties.backgroundPosition.type` | string |  |
| `schema.properties.template.properties.rows.items.properties.backgroundRepeat.type` | string |  |
| `schema.properties.template.properties.rows.items.properties.borderColor.type` | string |  |
| `schema.properties.template.properties.rows.items.properties.colStackOnMobile.type` | string |  |
| `schema.properties.template.properties.rows.items.properties.columns.items.additionalProperties` | boolean |  |
| `schema.properties.template.properties.rows.items.properties.columns.items.properties.backgroundColor.type` | string |  |
| `schema.properties.template.properties.rows.items.properties.columns.items.properties.borderColor.type` | string |  |
| `schema.properties.template.properties.rows.items.properties.columns.items.properties.customFields.type` | string |  |
| `schema.properties.template.properties.rows.items.properties.columns.items.properties.modules.items.discriminator.propertyName` | string |  |
| `schema.properties.template.properties.rows.items.properties.columns.items.properties.modules.items.oneOf[].additionalProperties` | boolean |  |
| `schema.properties.template.properties.rows.items.properties.columns.items.properties.modules.items.oneOf[].properties.align.enum[]` | string |  |
| `schema.properties.template.properties.rows.items.properties.columns.items.properties.modules.items.oneOf[].properties.backgroundColor.type` | string |  |
| `schema.properties.template.properties.rows.items.properties.columns.items.properties.modules.items.oneOf[].properties.borderColor.type` | string |  |
| `schema.properties.template.properties.rows.items.properties.columns.items.properties.modules.items.oneOf[].properties.color.type` | string |  |
| `schema.properties.template.properties.rows.items.properties.columns.items.properties.modules.items.oneOf[].properties.customFields.type` | string |  |
| `schema.properties.template.properties.rows.items.properties.columns.items.properties.modules.items.oneOf[].properties.hoverBackgroundColor.type` | string |  |
| `schema.properties.template.properties.rows.items.properties.columns.items.properties.modules.items.oneOf[].properties.hoverBorderColor.type` | string |  |
| `schema.properties.template.properties.rows.items.properties.columns.items.properties.modules.items.oneOf[].properties.hoverColor.type` | string |  |
| `schema.properties.template.properties.rows.items.properties.columns.items.properties.modules.items.oneOf[].properties.href.type` | string |  |
| `schema.properties.template.properties.rows.items.properties.columns.items.properties.modules.items.oneOf[].properties.label.format` | string |  |
| `schema.properties.template.properties.rows.items.properties.columns.items.properties.modules.items.oneOf[].properties.label.type` | string |  |
| `schema.properties.template.properties.rows.items.properties.columns.items.properties.modules.items.oneOf[].properties.locked.type` | string |  |
| `schema.properties.template.properties.rows.items.properties.columns.items.properties.modules.items.oneOf[].properties.size.minimum` | number |  |
| `schema.properties.template.properties.rows.items.properties.columns.items.properties.modules.items.oneOf[].properties.size.type` | string |  |
| `schema.properties.template.properties.rows.items.properties.columns.items.properties.modules.items.oneOf[].properties.target.enum[]` | string |  |
| `schema.properties.template.properties.rows.items.properties.columns.items.properties.modules.items.oneOf[].properties.text.format` | string |  |
| `schema.properties.template.properties.rows.items.properties.columns.items.properties.modules.items.oneOf[].properties.text.type` | string |  |
| `schema.properties.template.properties.rows.items.properties.columns.items.properties.modules.items.oneOf[].properties.type.const` | string |  |
| `schema.properties.template.properties.rows.items.properties.columns.items.properties.modules.items.oneOf[].title` | string |  |
| `schema.properties.template.properties.rows.items.properties.columns.items.properties.modules.items.oneOf[].type` | string |  |
| `schema.properties.template.properties.rows.items.properties.columns.items.properties.modules.items.required[]` | string |  |
| `schema.properties.template.properties.rows.items.properties.columns.items.properties.modules.items.type` | string |  |
| `schema.properties.template.properties.rows.items.properties.columns.items.properties.modules.type` | string |  |
| `schema.properties.template.properties.rows.items.properties.columns.items.properties.weight.maximum` | number |  |
| `schema.properties.template.properties.rows.items.properties.columns.items.properties.weight.minimum` | number |  |
| `schema.properties.template.properties.rows.items.properties.columns.items.properties.weight.type` | string |  |
| `schema.properties.template.properties.rows.items.properties.columns.items.required[]` | string |  |
| `schema.properties.template.properties.rows.items.properties.columns.items.title` | string |  |
| `schema.properties.template.properties.rows.items.properties.columns.items.type` | string |  |
| `schema.properties.template.properties.rows.items.properties.columns.maxItems` | number |  |
| `schema.properties.template.properties.rows.items.properties.columns.minItems` | number |  |
| `schema.properties.template.properties.rows.items.properties.columns.type` | string |  |
| `schema.properties.template.properties.rows.items.properties.columnsSpacing.maximum` | number |  |
| `schema.properties.template.properties.rows.items.properties.columnsSpacing.minimum` | number |  |
| `schema.properties.template.properties.rows.items.properties.columnsSpacing.type` | string |  |
| `schema.properties.template.properties.rows.items.properties.contentAreaBackgroundColor.type` | string |  |
| `schema.properties.template.properties.rows.items.properties.customFields.type` | string |  |
| `schema.properties.template.properties.rows.items.properties.displayCondition.properties.after.type` | string |  |
| `schema.properties.template.properties.rows.items.properties.displayCondition.properties.before.type` | string |  |
| `schema.properties.template.properties.rows.items.properties.displayCondition.properties.description.type` | string |  |
| `schema.properties.template.properties.rows.items.properties.displayCondition.properties.label.type` | string |  |
| `schema.properties.template.properties.rows.items.properties.displayCondition.properties.type.type` | string |  |
| `schema.properties.template.properties.rows.items.properties.displayCondition.required[]` | string |  |
| `schema.properties.template.properties.rows.items.properties.displayCondition.type` | string |  |
| `schema.properties.template.properties.rows.items.properties.locked.type` | string |  |
| `schema.properties.template.properties.rows.items.properties.metadata.type` | string |  |
| `schema.properties.template.properties.rows.items.properties.name.type` | string |  |
| `schema.properties.template.properties.rows.items.properties.rowReverseColStackOnMobile.type` | string |  |
| `schema.properties.template.properties.rows.items.properties.verticalAlign.enum[]` | string |  |
| `schema.properties.template.properties.rows.items.properties.verticalAlign.type` | string |  |
| `schema.properties.template.properties.rows.items.required[]` | string |  |
| `schema.properties.template.properties.rows.items.title` | string |  |
| `schema.properties.template.properties.rows.items.type` | string |  |
| `schema.properties.template.properties.rows.minItems` | number |  |
| `schema.properties.template.properties.rows.type` | string |  |
| `schema.properties.template.properties.settings.additionalProperties` | boolean |  |
| `schema.properties.template.properties.settings.properties.backgroundColor.type` | string |  |
| `schema.properties.template.properties.settings.properties.contentAreaBackgroundColor.type` | string |  |
| `schema.properties.template.properties.settings.properties.linkColor.type` | string |  |
| `schema.properties.template.properties.settings.properties.width.maximum` | number |  |
| `schema.properties.template.properties.settings.properties.width.minimum` | number |  |
| `schema.properties.template.properties.settings.properties.width.type` | string |  |
| `schema.properties.template.properties.settings.type` | string |  |
| `schema.properties.template.properties.type.enum[]` | string |  |
| `schema.properties.template.properties.type.type` | string |  |
| `schema.properties.template.required[]` | string |  |
| `schema.properties.template.type` | string |  |
| `schema.required[]` | string |  |
| `schema.title` | string |  |
| `schema.type` | string |  |

## Native endpoint

Through the native Easymailing API, this operation is `GET /templates-schema` (base URL `https://api.easymailing.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-template-schema.md) for the provider-specific parameters and requirements.

