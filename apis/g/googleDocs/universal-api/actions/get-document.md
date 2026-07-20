# Google Docs: Get Document

Retrieves a Google Docs document by ID.

```
GET https://connect.mindcloud.co/v1/universal/googleDocs/latest/actions/get-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Docs `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleDocs/latest/actions/get-document?connectionId=$CONNECTION_ID&documentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "documentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleDocs/latest/actions/get-document?${params}`, {
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
| `documentId` | list<string> | yes | ID of the document |

## Response

```json
{
  "success": true,
  "data": [
    {
      "body": {
        "content": [
          {
            "bullet": {
              "listId": "string"
            },
            "endIndex": 1,
            "paragraph": {
              "elements": [
                {
                  "startIndex": 1,
                  "textRun": {
                    "content": "string"
                  }
                }
              ],
              "paragraphStyle": {
                "direction": "string",
                "namedStyleType": "Ava Chen"
              }
            },
            "sectionBreak": {
              "sectionStyle": {
                "columnSeparatorStyle": "string",
                "contentDirection": "string",
                "sectionType": "string"
              }
            },
            "startIndex": 1
          }
        ]
      },
      "documentId": "string",
      "documentStyle": {
        "defaultHeaderId": "string",
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
      "headers": {
        "kix": {
          "wlpjykobduf8": {
            "content": [
              {
                "endIndex": 1,
                "paragraph": {
                  "elements": [
                    {
                      "endIndex": 1,
                      "textRun": {
                        "content": "string"
                      }
                    }
                  ],
                  "paragraphStyle": {
                    "direction": "string",
                    "namedStyleType": "Ava Chen"
                  }
                }
              }
            ],
            "headerId": "string"
          }
        }
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
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `body.content[].bullet.listId` | string | List identifier for bulleted paragraphs. |
| `body.content[].endIndex` | number |  |
| `body.content[].paragraph.elements[].startIndex` | number | Paragraph element start index. |
| `body.content[].paragraph.elements[].textRun.content` | string | Text run content. |
| `body.content[].paragraph.paragraphStyle.direction` | string | Paragraph text direction. |
| `body.content[].paragraph.paragraphStyle.namedStyleType` | string | Named paragraph style. |
| `body.content[].sectionBreak.sectionStyle.columnSeparatorStyle` | string |  |
| `body.content[].sectionBreak.sectionStyle.contentDirection` | string |  |
| `body.content[].sectionBreak.sectionStyle.sectionType` | string |  |
| `body.content[].startIndex` | number | Content element start index. |
| `documentId` | string |  |
| `documentStyle.defaultHeaderId` | string |  |
| `documentStyle.documentFormat.documentMode` | string | Document layout mode. |
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
| `headers.kix.wlpjykobduf8.content[].endIndex` | number |  |
| `headers.kix.wlpjykobduf8.content[].paragraph.elements[].endIndex` | number |  |
| `headers.kix.wlpjykobduf8.content[].paragraph.elements[].textRun.content` | string |  |
| `headers.kix.wlpjykobduf8.content[].paragraph.paragraphStyle.direction` | string |  |
| `headers.kix.wlpjykobduf8.content[].paragraph.paragraphStyle.namedStyleType` | string |  |
| `headers.kix.wlpjykobduf8.headerId` | string |  |
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
| `revisionId` | string | Opaque document revision identifier. |
| `suggestionsViewMode` | string |  |
| `title` | string |  |

## Native endpoint

Through the native Google Docs API, this operation is `GET /:documentId` (base URL `https://docs.googleapis.com/v1/documents`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-document.md) for the provider-specific parameters and requirements.

