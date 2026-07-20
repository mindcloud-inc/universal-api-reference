# Google Drive: Get Drive User (Auth)

Gets information about the authenticated user, the user's Drive, and system capabilities.

```
GET https://connect.mindcloud.co/v1/universal/googleDrive/latest/actions/get-drive-user-auth
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Drive `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleDrive/latest/actions/get-drive-user-auth?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleDrive/latest/actions/get-drive-user-auth?${params}`, {
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
| `fields` | string | no | Specify the fields to return for this method. (kind,user,storageQuota) Accepts multiple values as an array. Default: `*`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "appInstalled": true,
      "canCreateDrives": true,
      "canCreateTeamDrives": true,
      "driveThemes": [
        {
          "backgroundImageLink": "https://example.com",
          "colorRgb": "string",
          "id": "string"
        }
      ],
      "exportFormats": {
        "application/vnd": {
          "googleApps": {
            "document": [
              "string"
            ],
            "drawing": [
              "string"
            ],
            "form": [
              "string"
            ],
            "jam": [
              "string"
            ],
            "mailLayout": [
              "string"
            ],
            "presentation": [
              "string"
            ],
            "script": [
              "string"
            ],
            "site": [
              "string"
            ],
            "spreadsheet": [
              "string"
            ],
            "vid": [
              "string"
            ]
          }
        }
      },
      "folderColorPalette": [
        "string"
      ],
      "importFormats": {
        "application/msword": [
          "string"
        ],
        "application/pdf": [
          "string"
        ],
        "application/rtf": [
          "string"
        ],
        "application/vnd": {
          "googleApps": {
            "script+json": [
              "string"
            ],
            "script+text/plain": [
              "string"
            ]
          },
          "msExcel": {
            "sheet": {
              "macroenabled": {
                "12": [
                  "string"
                ]
              }
            },
            "template": {
              "macroenabled": {
                "12": [
                  "string"
                ]
              }
            }
          },
          "msPowerpoint": {
            "presentation": {
              "macroenabled": {
                "12": [
                  "string"
                ]
              }
            },
            "slideshow": {
              "macroenabled": {
                "12": [
                  "string"
                ]
              }
            },
            "template": {
              "macroenabled": {
                "12": [
                  "string"
                ]
              }
            }
          },
          "msWord": {
            "document": {
              "macroenabled": {
                "12": [
                  "string"
                ]
              }
            },
            "template": {
              "macroenabled": {
                "12": [
                  "string"
                ]
              }
            }
          },
          "oasis": {
            "opendocument": {
              "presentation": [
                "string"
              ],
              "spreadsheet": [
                "string"
              ],
              "text": [
                "string"
              ]
            }
          },
          "openxmlformatsOfficedocument": {
            "presentationml": {
              "presentation": [
                "string"
              ],
              "slideshow": [
                "string"
              ],
              "template": [
                "string"
              ]
            },
            "spreadsheetml": {
              "sheet": [
                "string"
              ],
              "template": [
                "string"
              ]
            },
            "wordprocessingml": {
              "document": [
                "string"
              ],
              "template": [
                "string"
              ]
            }
          },
          "sun": {
            "xml": {
              "writer": [
                "string"
              ]
            }
          }
        },
        "application/xMsmetafile": [
          "string"
        ],
        "application/xVnd": {
          "oasis": {
            "opendocument": {
              "presentation": [
                "string"
              ],
              "spreadsheet": [
                "string"
              ],
              "text": [
                "string"
              ]
            }
          }
        },
        "image/bmp": [
          "string"
        ],
        "image/gif": [
          "string"
        ],
        "image/jpeg": [
          "string"
        ],
        "image/jpg": [
          "string"
        ],
        "image/pjpeg": [
          "string"
        ],
        "image/png": [
          "string"
        ],
        "image/xBmp": [
          "string"
        ],
        "image/xPng": [
          "string"
        ],
        "text/csv": [
          "string"
        ],
        "text/html": [
          "string"
        ],
        "text/markdown": [
          "string"
        ],
        "text/plain": [
          "string"
        ],
        "text/richtext": [
          "string"
        ],
        "text/rtf": [
          "string"
        ],
        "text/tabSeparatedValues": [
          "string"
        ],
        "text/xMarkdown": [
          "string"
        ]
      },
      "kind": "string",
      "maxImportSizes": {
        "application/vnd": {
          "googleApps": {
            "document": "string",
            "drawing": "string",
            "presentation": "string",
            "spreadsheet": "string"
          }
        }
      },
      "maxUploadSize": "string",
      "storageQuota": {
        "limit": "string",
        "usage": "string",
        "usageInDrive": "string",
        "usageInDriveTrash": "string"
      },
      "teamDriveThemes": [
        {
          "backgroundImageLink": "https://example.com",
          "colorRgb": "string",
          "id": "string"
        }
      ],
      "user": {
        "displayName": "Ava Chen",
        "emailAddress": "ava@example.com",
        "kind": "string",
        "me": true,
        "permissionId": "string",
        "photoLink": "https://example.com"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `appInstalled` | boolean |  |
| `canCreateDrives` | boolean |  |
| `canCreateTeamDrives` | boolean |  |
| `driveThemes[].backgroundImageLink` | string |  |
| `driveThemes[].colorRgb` | string |  |
| `driveThemes[].id` | string |  |
| `exportFormats.application/vnd.googleApps.document[]` | string |  |
| `exportFormats.application/vnd.googleApps.drawing[]` | string |  |
| `exportFormats.application/vnd.googleApps.form[]` | string |  |
| `exportFormats.application/vnd.googleApps.jam[]` | string |  |
| `exportFormats.application/vnd.googleApps.mailLayout[]` | string |  |
| `exportFormats.application/vnd.googleApps.presentation[]` | string |  |
| `exportFormats.application/vnd.googleApps.script[]` | string |  |
| `exportFormats.application/vnd.googleApps.site[]` | string |  |
| `exportFormats.application/vnd.googleApps.spreadsheet[]` | string |  |
| `exportFormats.application/vnd.googleApps.vid[]` | string |  |
| `folderColorPalette[]` | string |  |
| `importFormats.application/msword[]` | string |  |
| `importFormats.application/pdf[]` | string |  |
| `importFormats.application/rtf[]` | string |  |
| `importFormats.application/vnd.googleApps.script+json[]` | string |  |
| `importFormats.application/vnd.googleApps.script+text/plain[]` | string |  |
| `importFormats.application/vnd.msExcel.sheet.macroenabled.12[]` | string |  |
| `importFormats.application/vnd.msExcel.template.macroenabled.12[]` | string |  |
| `importFormats.application/vnd.msExcel[]` | string |  |
| `importFormats.application/vnd.msPowerpoint.presentation.macroenabled.12[]` | string |  |
| `importFormats.application/vnd.msPowerpoint.slideshow.macroenabled.12[]` | string |  |
| `importFormats.application/vnd.msPowerpoint.template.macroenabled.12[]` | string |  |
| `importFormats.application/vnd.msPowerpoint[]` | string |  |
| `importFormats.application/vnd.msWord.document.macroenabled.12[]` | string |  |
| `importFormats.application/vnd.msWord.template.macroenabled.12[]` | string |  |
| `importFormats.application/vnd.oasis.opendocument.presentation[]` | string |  |
| `importFormats.application/vnd.oasis.opendocument.spreadsheet[]` | string |  |
| `importFormats.application/vnd.oasis.opendocument.text[]` | string |  |
| `importFormats.application/vnd.openxmlformatsOfficedocument.presentationml.presentation[]` | string |  |
| `importFormats.application/vnd.openxmlformatsOfficedocument.presentationml.slideshow[]` | string |  |
| `importFormats.application/vnd.openxmlformatsOfficedocument.presentationml.template[]` | string |  |
| `importFormats.application/vnd.openxmlformatsOfficedocument.spreadsheetml.sheet[]` | string |  |
| `importFormats.application/vnd.openxmlformatsOfficedocument.spreadsheetml.template[]` | string |  |
| `importFormats.application/vnd.openxmlformatsOfficedocument.wordprocessingml.document[]` | string |  |
| `importFormats.application/vnd.openxmlformatsOfficedocument.wordprocessingml.template[]` | string |  |
| `importFormats.application/vnd.sun.xml.writer[]` | string |  |
| `importFormats.application/xMsmetafile[]` | string |  |
| `importFormats.application/xVnd.oasis.opendocument.presentation[]` | string |  |
| `importFormats.application/xVnd.oasis.opendocument.spreadsheet[]` | string |  |
| `importFormats.application/xVnd.oasis.opendocument.text[]` | string |  |
| `importFormats.image/bmp[]` | string |  |
| `importFormats.image/gif[]` | string |  |
| `importFormats.image/jpeg[]` | string |  |
| `importFormats.image/jpg[]` | string |  |
| `importFormats.image/pjpeg[]` | string |  |
| `importFormats.image/png[]` | string |  |
| `importFormats.image/xBmp[]` | string |  |
| `importFormats.image/xPng[]` | string |  |
| `importFormats.text/csv[]` | string |  |
| `importFormats.text/html[]` | string |  |
| `importFormats.text/markdown[]` | string |  |
| `importFormats.text/plain[]` | string |  |
| `importFormats.text/richtext[]` | string |  |
| `importFormats.text/rtf[]` | string |  |
| `importFormats.text/tabSeparatedValues[]` | string |  |
| `importFormats.text/xMarkdown[]` | string |  |
| `kind` | string |  |
| `maxImportSizes.application/vnd.googleApps.document` | string |  |
| `maxImportSizes.application/vnd.googleApps.drawing` | string |  |
| `maxImportSizes.application/vnd.googleApps.presentation` | string |  |
| `maxImportSizes.application/vnd.googleApps.spreadsheet` | string |  |
| `maxUploadSize` | string |  |
| `storageQuota.limit` | string |  |
| `storageQuota.usage` | string |  |
| `storageQuota.usageInDrive` | string |  |
| `storageQuota.usageInDriveTrash` | string |  |
| `teamDriveThemes[].backgroundImageLink` | string |  |
| `teamDriveThemes[].colorRgb` | string |  |
| `teamDriveThemes[].id` | string |  |
| `user.displayName` | string |  |
| `user.emailAddress` | string |  |
| `user.kind` | string |  |
| `user.me` | boolean |  |
| `user.permissionId` | string |  |
| `user.photoLink` | string |  |

## Native endpoint

Through the native Google Drive API, this operation is `GET /drive/v3/about` (base URL `https://www.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-drive-user-auth.md) for the provider-specific parameters and requirements.

