# Google Docs: Create Blank Document

Creates a new blank document in Google Docs.

```
POST https://connect.mindcloud.co/v1/universal/googleDocs/latest/actions/create-blank-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Docs `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/googleDocs/latest/actions/create-blank-document" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/googleDocs/latest/actions/create-blank-document', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `title` | string | no | Title of the new document |

## Response

```json
{
  "success": true,
  "data": [
    {
      "body": {
        "content": [
          {
            "endIndex": 1,
            "sectionBreak": {
              "sectionStyle": {
                "columnSeparatorStyle": "string",
                "contentDirection": "string",
                "sectionType": "string"
              }
            }
          }
        ]
      },
      "documentId": "string",
      "documentStyle": {
        "documentFormat": {
          "documentMode": "string"
        },
        "marginBottom": {
          "magnitude": 1,
          "unit": "string"
        },
        "marginFooter": {
          "magnitude": 1,
          "unit": "string"
        },
        "marginHeader": {
          "magnitude": 1,
          "unit": "string"
        },
        "marginLeft": {
          "magnitude": 1,
          "unit": "string"
        },
        "marginRight": {
          "magnitude": 1,
          "unit": "string"
        },
        "marginTop": {
          "magnitude": 1,
          "unit": "string"
        },
        "pageNumberStart": 1,
        "pageSize": {
          "height": {
            "magnitude": 1,
            "unit": "string"
          },
          "width": {
            "magnitude": 1,
            "unit": "string"
          }
        },
        "useCustomHeaderFooterMargins": true
      },
      "namedStyles": {
        "styles": [
          {
            "namedStyleType": "Ava Chen",
            "paragraphStyle": {
              "alignment": "Ava Chen",
              "avoidWidowAndOrphan": true,
              "borderBetween": {
                "dashStyle": "Ava Chen",
                "padding": {
                  "unit": "Ava Chen"
                },
                "width": {
                  "unit": "Ava Chen"
                }
              },
              "borderBottom": {
                "dashStyle": "Ava Chen",
                "padding": {
                  "unit": "Ava Chen"
                },
                "width": {
                  "unit": "Ava Chen"
                }
              },
              "borderLeft": {
                "dashStyle": "Ava Chen",
                "padding": {
                  "unit": "Ava Chen"
                },
                "width": {
                  "unit": "Ava Chen"
                }
              },
              "borderRight": {
                "dashStyle": "Ava Chen",
                "padding": {
                  "unit": "Ava Chen"
                },
                "width": {
                  "unit": "Ava Chen"
                }
              },
              "borderTop": {
                "dashStyle": "Ava Chen",
                "padding": {
                  "unit": "Ava Chen"
                },
                "width": {
                  "unit": "Ava Chen"
                }
              },
              "direction": "Ava Chen",
              "indentEnd": {
                "unit": "Ava Chen"
              },
              "indentFirstLine": {
                "unit": "Ava Chen"
              },
              "indentStart": {
                "unit": "Ava Chen"
              },
              "keepLinesTogether": true,
              "keepWithNext": true,
              "lineSpacing": 1,
              "namedStyleType": "Ava Chen",
              "pageBreakBefore": true,
              "spaceAbove": {
                "unit": "Ava Chen"
              },
              "spaceBelow": {
                "unit": "Ava Chen"
              },
              "spacingMode": "Ava Chen"
            },
            "textStyle": {
              "baselineOffset": "Ava Chen",
              "bold": true,
              "fontSize": {
                "magnitude": 1,
                "unit": "Ava Chen"
              },
              "italic": true,
              "smallCaps": true,
              "strikethrough": true,
              "underline": true,
              "weightedFontFamily": {
                "fontFamily": "Ava Chen",
                "weight": 1
              }
            }
          }
        ]
      },
      "revisionId": "string",
      "suggestionsViewMode": "string",
      "tabs": [
        {
          "documentTab": {
            "body": {
              "content": [
                {
                  "endIndex": 1,
                  "sectionBreak": {
                    "sectionStyle": {
                      "columnSeparatorStyle": "string",
                      "contentDirection": "string",
                      "sectionType": "string"
                    }
                  }
                }
              ]
            },
            "documentStyle": {
              "documentFormat": {
                "documentMode": "string"
              },
              "marginBottom": {
                "magnitude": 1,
                "unit": "string"
              },
              "marginFooter": {
                "magnitude": 1,
                "unit": "string"
              },
              "marginHeader": {
                "magnitude": 1,
                "unit": "string"
              },
              "marginLeft": {
                "magnitude": 1,
                "unit": "string"
              },
              "marginRight": {
                "magnitude": 1,
                "unit": "string"
              },
              "marginTop": {
                "magnitude": 1,
                "unit": "string"
              },
              "pageNumberStart": 1,
              "pageSize": {
                "height": {
                  "magnitude": 1,
                  "unit": "string"
                },
                "width": {
                  "magnitude": 1,
                  "unit": "string"
                }
              },
              "useCustomHeaderFooterMargins": true
            },
            "namedStyles": {
              "styles": [
                {
                  "namedStyleType": "Ava Chen",
                  "paragraphStyle": {
                    "alignment": "Ava Chen",
                    "avoidWidowAndOrphan": true,
                    "borderBetween": {
                      "dashStyle": "Ava Chen",
                      "padding": {
                        "unit": "Ava Chen"
                      },
                      "width": {
                        "unit": "Ava Chen"
                      }
                    },
                    "borderBottom": {
                      "dashStyle": "Ava Chen",
                      "padding": {
                        "unit": "Ava Chen"
                      },
                      "width": {
                        "unit": "Ava Chen"
                      }
                    },
                    "borderLeft": {
                      "dashStyle": "Ava Chen",
                      "padding": {
                        "unit": "Ava Chen"
                      },
                      "width": {
                        "unit": "Ava Chen"
                      }
                    },
                    "borderRight": {
                      "dashStyle": "Ava Chen",
                      "padding": {
                        "unit": "Ava Chen"
                      },
                      "width": {
                        "unit": "Ava Chen"
                      }
                    },
                    "borderTop": {
                      "dashStyle": "Ava Chen",
                      "padding": {
                        "unit": "Ava Chen"
                      },
                      "width": {
                        "unit": "Ava Chen"
                      }
                    },
                    "direction": "Ava Chen",
                    "indentEnd": {
                      "unit": "Ava Chen"
                    },
                    "indentFirstLine": {
                      "unit": "Ava Chen"
                    },
                    "indentStart": {
                      "unit": "Ava Chen"
                    },
                    "keepLinesTogether": true,
                    "keepWithNext": true,
                    "lineSpacing": 1,
                    "namedStyleType": "Ava Chen",
                    "pageBreakBefore": true,
                    "spaceAbove": {
                      "unit": "Ava Chen"
                    },
                    "spaceBelow": {
                      "unit": "Ava Chen"
                    },
                    "spacingMode": "Ava Chen"
                  },
                  "textStyle": {
                    "baselineOffset": "Ava Chen",
                    "bold": true,
                    "fontSize": {
                      "magnitude": 1,
                      "unit": "Ava Chen"
                    },
                    "italic": true,
                    "smallCaps": true,
                    "strikethrough": true,
                    "underline": true,
                    "weightedFontFamily": {
                      "fontFamily": "Ava Chen",
                      "weight": 1
                    }
                  }
                }
              ]
            }
          },
          "tabProperties": {
            "index": 1,
            "tabId": "string",
            "title": "string"
          }
        }
      ],
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `body.content[].endIndex` | number |  |
| `body.content[].sectionBreak.sectionStyle.columnSeparatorStyle` | string |  |
| `body.content[].sectionBreak.sectionStyle.contentDirection` | string |  |
| `body.content[].sectionBreak.sectionStyle.sectionType` | string |  |
| `documentId` | string |  |
| `documentStyle.documentFormat.documentMode` | string |  |
| `documentStyle.marginBottom.magnitude` | number |  |
| `documentStyle.marginBottom.unit` | string |  |
| `documentStyle.marginFooter.magnitude` | number |  |
| `documentStyle.marginFooter.unit` | string |  |
| `documentStyle.marginHeader.magnitude` | number |  |
| `documentStyle.marginHeader.unit` | string |  |
| `documentStyle.marginLeft.magnitude` | number |  |
| `documentStyle.marginLeft.unit` | string |  |
| `documentStyle.marginRight.magnitude` | number |  |
| `documentStyle.marginRight.unit` | string |  |
| `documentStyle.marginTop.magnitude` | number |  |
| `documentStyle.marginTop.unit` | string |  |
| `documentStyle.pageNumberStart` | number |  |
| `documentStyle.pageSize.height.magnitude` | number |  |
| `documentStyle.pageSize.height.unit` | string |  |
| `documentStyle.pageSize.width.magnitude` | number |  |
| `documentStyle.pageSize.width.unit` | string |  |
| `documentStyle.useCustomHeaderFooterMargins` | boolean |  |
| `namedStyles.styles[].namedStyleType` | string |  |
| `namedStyles.styles[].paragraphStyle.alignment` | string |  |
| `namedStyles.styles[].paragraphStyle.avoidWidowAndOrphan` | boolean |  |
| `namedStyles.styles[].paragraphStyle.borderBetween.dashStyle` | string |  |
| `namedStyles.styles[].paragraphStyle.borderBetween.padding.unit` | string |  |
| `namedStyles.styles[].paragraphStyle.borderBetween.width.unit` | string |  |
| `namedStyles.styles[].paragraphStyle.borderBottom.dashStyle` | string |  |
| `namedStyles.styles[].paragraphStyle.borderBottom.padding.unit` | string |  |
| `namedStyles.styles[].paragraphStyle.borderBottom.width.unit` | string |  |
| `namedStyles.styles[].paragraphStyle.borderLeft.dashStyle` | string |  |
| `namedStyles.styles[].paragraphStyle.borderLeft.padding.unit` | string |  |
| `namedStyles.styles[].paragraphStyle.borderLeft.width.unit` | string |  |
| `namedStyles.styles[].paragraphStyle.borderRight.dashStyle` | string |  |
| `namedStyles.styles[].paragraphStyle.borderRight.padding.unit` | string |  |
| `namedStyles.styles[].paragraphStyle.borderRight.width.unit` | string |  |
| `namedStyles.styles[].paragraphStyle.borderTop.dashStyle` | string |  |
| `namedStyles.styles[].paragraphStyle.borderTop.padding.unit` | string |  |
| `namedStyles.styles[].paragraphStyle.borderTop.width.unit` | string |  |
| `namedStyles.styles[].paragraphStyle.direction` | string |  |
| `namedStyles.styles[].paragraphStyle.indentEnd.unit` | string |  |
| `namedStyles.styles[].paragraphStyle.indentFirstLine.unit` | string |  |
| `namedStyles.styles[].paragraphStyle.indentStart.unit` | string |  |
| `namedStyles.styles[].paragraphStyle.keepLinesTogether` | boolean |  |
| `namedStyles.styles[].paragraphStyle.keepWithNext` | boolean |  |
| `namedStyles.styles[].paragraphStyle.lineSpacing` | number |  |
| `namedStyles.styles[].paragraphStyle.namedStyleType` | string |  |
| `namedStyles.styles[].paragraphStyle.pageBreakBefore` | boolean |  |
| `namedStyles.styles[].paragraphStyle.spaceAbove.unit` | string |  |
| `namedStyles.styles[].paragraphStyle.spaceBelow.unit` | string |  |
| `namedStyles.styles[].paragraphStyle.spacingMode` | string |  |
| `namedStyles.styles[].textStyle.baselineOffset` | string |  |
| `namedStyles.styles[].textStyle.bold` | boolean |  |
| `namedStyles.styles[].textStyle.fontSize.magnitude` | number |  |
| `namedStyles.styles[].textStyle.fontSize.unit` | string |  |
| `namedStyles.styles[].textStyle.italic` | boolean |  |
| `namedStyles.styles[].textStyle.smallCaps` | boolean |  |
| `namedStyles.styles[].textStyle.strikethrough` | boolean |  |
| `namedStyles.styles[].textStyle.underline` | boolean |  |
| `namedStyles.styles[].textStyle.weightedFontFamily.fontFamily` | string |  |
| `namedStyles.styles[].textStyle.weightedFontFamily.weight` | number |  |
| `revisionId` | string |  |
| `suggestionsViewMode` | string |  |
| `tabs[].documentTab.body.content[].endIndex` | number |  |
| `tabs[].documentTab.body.content[].sectionBreak.sectionStyle.columnSeparatorStyle` | string |  |
| `tabs[].documentTab.body.content[].sectionBreak.sectionStyle.contentDirection` | string |  |
| `tabs[].documentTab.body.content[].sectionBreak.sectionStyle.sectionType` | string |  |
| `tabs[].documentTab.documentStyle.documentFormat.documentMode` | string |  |
| `tabs[].documentTab.documentStyle.marginBottom.magnitude` | number |  |
| `tabs[].documentTab.documentStyle.marginBottom.unit` | string |  |
| `tabs[].documentTab.documentStyle.marginFooter.magnitude` | number |  |
| `tabs[].documentTab.documentStyle.marginFooter.unit` | string |  |
| `tabs[].documentTab.documentStyle.marginHeader.magnitude` | number |  |
| `tabs[].documentTab.documentStyle.marginHeader.unit` | string |  |
| `tabs[].documentTab.documentStyle.marginLeft.magnitude` | number |  |
| `tabs[].documentTab.documentStyle.marginLeft.unit` | string |  |
| `tabs[].documentTab.documentStyle.marginRight.magnitude` | number |  |
| `tabs[].documentTab.documentStyle.marginRight.unit` | string |  |
| `tabs[].documentTab.documentStyle.marginTop.magnitude` | number |  |
| `tabs[].documentTab.documentStyle.marginTop.unit` | string |  |
| `tabs[].documentTab.documentStyle.pageNumberStart` | number |  |
| `tabs[].documentTab.documentStyle.pageSize.height.magnitude` | number |  |
| `tabs[].documentTab.documentStyle.pageSize.height.unit` | string |  |
| `tabs[].documentTab.documentStyle.pageSize.width.magnitude` | number |  |
| `tabs[].documentTab.documentStyle.pageSize.width.unit` | string |  |
| `tabs[].documentTab.documentStyle.useCustomHeaderFooterMargins` | boolean |  |
| `tabs[].documentTab.namedStyles.styles[].namedStyleType` | string |  |
| `tabs[].documentTab.namedStyles.styles[].paragraphStyle.alignment` | string |  |
| `tabs[].documentTab.namedStyles.styles[].paragraphStyle.avoidWidowAndOrphan` | boolean |  |
| `tabs[].documentTab.namedStyles.styles[].paragraphStyle.borderBetween.dashStyle` | string |  |
| `tabs[].documentTab.namedStyles.styles[].paragraphStyle.borderBetween.padding.unit` | string |  |
| `tabs[].documentTab.namedStyles.styles[].paragraphStyle.borderBetween.width.unit` | string |  |
| `tabs[].documentTab.namedStyles.styles[].paragraphStyle.borderBottom.dashStyle` | string |  |
| `tabs[].documentTab.namedStyles.styles[].paragraphStyle.borderBottom.padding.unit` | string |  |
| `tabs[].documentTab.namedStyles.styles[].paragraphStyle.borderBottom.width.unit` | string |  |
| `tabs[].documentTab.namedStyles.styles[].paragraphStyle.borderLeft.dashStyle` | string |  |
| `tabs[].documentTab.namedStyles.styles[].paragraphStyle.borderLeft.padding.unit` | string |  |
| `tabs[].documentTab.namedStyles.styles[].paragraphStyle.borderLeft.width.unit` | string |  |
| `tabs[].documentTab.namedStyles.styles[].paragraphStyle.borderRight.dashStyle` | string |  |
| `tabs[].documentTab.namedStyles.styles[].paragraphStyle.borderRight.padding.unit` | string |  |
| `tabs[].documentTab.namedStyles.styles[].paragraphStyle.borderRight.width.unit` | string |  |
| `tabs[].documentTab.namedStyles.styles[].paragraphStyle.borderTop.dashStyle` | string |  |
| `tabs[].documentTab.namedStyles.styles[].paragraphStyle.borderTop.padding.unit` | string |  |
| `tabs[].documentTab.namedStyles.styles[].paragraphStyle.borderTop.width.unit` | string |  |
| `tabs[].documentTab.namedStyles.styles[].paragraphStyle.direction` | string |  |
| `tabs[].documentTab.namedStyles.styles[].paragraphStyle.indentEnd.unit` | string |  |
| `tabs[].documentTab.namedStyles.styles[].paragraphStyle.indentFirstLine.unit` | string |  |
| `tabs[].documentTab.namedStyles.styles[].paragraphStyle.indentStart.unit` | string |  |
| `tabs[].documentTab.namedStyles.styles[].paragraphStyle.keepLinesTogether` | boolean |  |
| `tabs[].documentTab.namedStyles.styles[].paragraphStyle.keepWithNext` | boolean |  |
| `tabs[].documentTab.namedStyles.styles[].paragraphStyle.lineSpacing` | number |  |
| `tabs[].documentTab.namedStyles.styles[].paragraphStyle.namedStyleType` | string |  |
| `tabs[].documentTab.namedStyles.styles[].paragraphStyle.pageBreakBefore` | boolean |  |
| `tabs[].documentTab.namedStyles.styles[].paragraphStyle.spaceAbove.unit` | string |  |
| `tabs[].documentTab.namedStyles.styles[].paragraphStyle.spaceBelow.unit` | string |  |
| `tabs[].documentTab.namedStyles.styles[].paragraphStyle.spacingMode` | string |  |
| `tabs[].documentTab.namedStyles.styles[].textStyle.baselineOffset` | string |  |
| `tabs[].documentTab.namedStyles.styles[].textStyle.bold` | boolean |  |
| `tabs[].documentTab.namedStyles.styles[].textStyle.fontSize.magnitude` | number |  |
| `tabs[].documentTab.namedStyles.styles[].textStyle.fontSize.unit` | string |  |
| `tabs[].documentTab.namedStyles.styles[].textStyle.italic` | boolean |  |
| `tabs[].documentTab.namedStyles.styles[].textStyle.smallCaps` | boolean |  |
| `tabs[].documentTab.namedStyles.styles[].textStyle.strikethrough` | boolean |  |
| `tabs[].documentTab.namedStyles.styles[].textStyle.underline` | boolean |  |
| `tabs[].documentTab.namedStyles.styles[].textStyle.weightedFontFamily.fontFamily` | string |  |
| `tabs[].documentTab.namedStyles.styles[].textStyle.weightedFontFamily.weight` | number |  |
| `tabs[].tabProperties.index` | number |  |
| `tabs[].tabProperties.tabId` | string |  |
| `tabs[].tabProperties.title` | string |  |
| `title` | string |  |

## Native endpoint

Through the native Google Docs API, this operation is `POST /` (base URL `https://docs.googleapis.com/v1/documents`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-blank-document.md) for the provider-specific parameters and requirements.

