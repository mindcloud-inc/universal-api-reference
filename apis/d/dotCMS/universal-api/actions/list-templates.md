# DotCMS: List Templates

Retrieves available template records from DotCMS.

```
GET https://connect.mindcloud.co/v1/universal/dotCMS/latest/actions/list-templates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DotCMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dotCMS/latest/actions/list-templates?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dotCMS/latest/actions/list-templates?${params}`, {
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
      "entity": [
        {
          "body": {},
          "canPublish": true,
          "canRead": true,
          "canWrite": true,
          "categoryId": "string",
          "countAddContainer": 1,
          "countContainers": 1,
          "deleted": true,
          "drawed": true,
          "drawedBody": "string",
          "footer": {},
          "friendlyName": "Ava Chen",
          "fullTitle": "string",
          "hasLiveVersion": true,
          "headCode": {},
          "header": {},
          "hostId": "string",
          "hostName": "Ava Chen",
          "htmlTitle": "string",
          "identifier": "string",
          "image": "string",
          "inode": "string",
          "layout": {
            "body": {
              "rows": [
                {
                  "columns": [
                    {
                      "containers": [
                        {
                          "historyUUIDs": [
                            "string"
                          ],
                          "identifier": "string",
                          "uuid": "string"
                        }
                      ],
                      "leftOffset": 1,
                      "styleClass": "string",
                      "width": 1
                    }
                  ],
                  "styleClass": "string"
                }
              ]
            },
            "footer": true,
            "header": true,
            "sidebar": {},
            "title": {},
            "width": {}
          },
          "live": true,
          "locked": true,
          "lockedBy": {},
          "modDate": "2026-05-07T12:00:00.000Z",
          "modUser": "string",
          "name": "Ava Chen",
          "new": true,
          "owner": "string",
          "selectedimage": {},
          "showOnMenu": true,
          "sortOrder": 1,
          "theme": "string",
          "themeInfo": {
            "defaultFileType": {},
            "filesMasks": {},
            "hostId": "string",
            "iDate": {},
            "identifier": "string",
            "inode": "string",
            "modDate": "2026-05-07T12:00:00.000Z",
            "name": "Ava Chen",
            "path": "string",
            "showOnMenu": true,
            "sortOrder": 1,
            "title": "string",
            "type": "string"
          },
          "themeName": "Ava Chen",
          "title": "string",
          "working": true
        }
      ],
      "pagination": {
        "currentPage": 1,
        "perPage": 1,
        "totalEntries": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `entity[].body` | object |  |
| `entity[].canPublish` | boolean |  |
| `entity[].canRead` | boolean |  |
| `entity[].canWrite` | boolean |  |
| `entity[].categoryId` | string |  |
| `entity[].countAddContainer` | number |  |
| `entity[].countContainers` | number |  |
| `entity[].deleted` | boolean |  |
| `entity[].drawed` | boolean |  |
| `entity[].drawedBody` | string |  |
| `entity[].footer` | object |  |
| `entity[].friendlyName` | string |  |
| `entity[].fullTitle` | string |  |
| `entity[].hasLiveVersion` | boolean |  |
| `entity[].headCode` | object |  |
| `entity[].header` | object |  |
| `entity[].hostId` | string |  |
| `entity[].hostName` | string |  |
| `entity[].htmlTitle` | string |  |
| `entity[].identifier` | string |  |
| `entity[].image` | string |  |
| `entity[].inode` | string |  |
| `entity[].layout.body.rows[].columns[].containers[].historyUUIDs[]` | string |  |
| `entity[].layout.body.rows[].columns[].containers[].identifier` | string |  |
| `entity[].layout.body.rows[].columns[].containers[].uuid` | string |  |
| `entity[].layout.body.rows[].columns[].leftOffset` | number |  |
| `entity[].layout.body.rows[].columns[].styleClass` | string |  |
| `entity[].layout.body.rows[].columns[].width` | number |  |
| `entity[].layout.body.rows[].styleClass` | string |  |
| `entity[].layout.footer` | boolean |  |
| `entity[].layout.header` | boolean |  |
| `entity[].layout.sidebar` | object |  |
| `entity[].layout.title` | object |  |
| `entity[].layout.width` | object |  |
| `entity[].live` | boolean |  |
| `entity[].locked` | boolean |  |
| `entity[].lockedBy` | object |  |
| `entity[].modDate` | date |  |
| `entity[].modUser` | string |  |
| `entity[].name` | string |  |
| `entity[].new` | boolean |  |
| `entity[].owner` | string |  |
| `entity[].selectedimage` | object |  |
| `entity[].showOnMenu` | boolean |  |
| `entity[].sortOrder` | number |  |
| `entity[].theme` | string |  |
| `entity[].themeInfo.defaultFileType` | object |  |
| `entity[].themeInfo.filesMasks` | object |  |
| `entity[].themeInfo.hostId` | string |  |
| `entity[].themeInfo.iDate` | object |  |
| `entity[].themeInfo.identifier` | string |  |
| `entity[].themeInfo.inode` | string |  |
| `entity[].themeInfo.modDate` | date |  |
| `entity[].themeInfo.name` | string |  |
| `entity[].themeInfo.path` | string |  |
| `entity[].themeInfo.showOnMenu` | boolean |  |
| `entity[].themeInfo.sortOrder` | number |  |
| `entity[].themeInfo.title` | string |  |
| `entity[].themeInfo.type` | string |  |
| `entity[].themeName` | string |  |
| `entity[].title` | string |  |
| `entity[].working` | boolean |  |
| `pagination.currentPage` | number |  |
| `pagination.perPage` | number |  |
| `pagination.totalEntries` | number |  |

## Native endpoint

Through the native DotCMS API, this operation is `GET /api/v1/templates` (base URL `https://demo.dotcms.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-templates.md) for the provider-specific parameters and requirements.

