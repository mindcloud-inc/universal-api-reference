# Google Docs Universal API Examples

These examples use the MindCloud API key and Google Docs connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Documents

Finds Google Docs and Word documents in Google Drive.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleDocs/latest/actions/list-documents?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleDocs/latest/actions/list-documents?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "mimeType": "string",
      "name": "Ava Chen",
      "parents": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

See the full [List Documents action reference](actions/list-documents.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/googleDocs/latest/actions/list-documents).

## Create Blank Document

Creates a new blank document in Google Docs.

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

Example response:

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

See the full [Create Blank Document action reference](actions/create-blank-document.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/googleDocs/latest/actions/create-blank-document).
