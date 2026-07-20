# SmartSuite: List Solutions

Retrieves solutions from SmartSuite.

```
GET https://connect.mindcloud.co/v1/universal/smartSuite/latest/actions/list-solutions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SmartSuite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smartSuite/latest/actions/list-solutions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smartSuite/latest/actions/list-solutions?${params}`, {
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
      "applicationsCount": 1,
      "automationCount": 1,
      "created": "string",
      "createdBy": "string",
      "deleteDate": {},
      "deletedBy": {},
      "description": {
        "data": {
          "content": [
            {
              "attrs": {
                "collapse": true,
                "id": "string",
                "indentation": {},
                "level": 1,
                "textAlign": "string"
              },
              "content": [
                {
                  "text": "string",
                  "type": "string"
                }
              ],
              "type": "string"
            }
          ],
          "type": "string"
        },
        "html": "string",
        "preview": "string"
      },
      "hasDemoData": true,
      "hidden": true,
      "homepageCategory": "string",
      "homepageCategoryName": "Ava Chen",
      "homepageCategoryOrder": {},
      "id": "string",
      "lastAccess": {},
      "logoColor": "string",
      "logoIcon": "string",
      "membersCount": 1,
      "name": "Ava Chen",
      "permissions": {
        "level": "string",
        "owners": [
          "string"
        ],
        "privateTo": "string"
      },
      "recordsCount": 1,
      "sharingAllowCopy": true,
      "sharingEnabled": true,
      "sharingHash": "string",
      "sharingPassword": "string",
      "slug": "string",
      "status": "string",
      "template": "string",
      "updated": "string",
      "updatedBy": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `applicationsCount` | number |  |
| `automationCount` | number |  |
| `created` | string |  |
| `createdBy` | string |  |
| `deleteDate` | object |  |
| `deletedBy` | object |  |
| `description.data.content[].attrs.collapse` | boolean |  |
| `description.data.content[].attrs.id` | string |  |
| `description.data.content[].attrs.indentation` | object |  |
| `description.data.content[].attrs.level` | number |  |
| `description.data.content[].attrs.textAlign` | string |  |
| `description.data.content[].content[].text` | string |  |
| `description.data.content[].content[].type` | string |  |
| `description.data.content[].type` | string |  |
| `description.data.type` | string |  |
| `description.html` | string |  |
| `description.preview` | string |  |
| `hasDemoData` | boolean |  |
| `hidden` | boolean |  |
| `homepageCategory` | string |  |
| `homepageCategoryName` | string |  |
| `homepageCategoryOrder` | object |  |
| `id` | string |  |
| `lastAccess` | object |  |
| `logoColor` | string |  |
| `logoIcon` | string |  |
| `membersCount` | number |  |
| `name` | string |  |
| `permissions.level` | string |  |
| `permissions.owners[]` | string |  |
| `permissions.privateTo` | string |  |
| `recordsCount` | number |  |
| `sharingAllowCopy` | boolean |  |
| `sharingEnabled` | boolean |  |
| `sharingHash` | string |  |
| `sharingPassword` | string |  |
| `slug` | string |  |
| `status` | string |  |
| `template` | string |  |
| `updated` | string |  |
| `updatedBy` | string |  |

## Native endpoint

Through the native SmartSuite API, this operation is `GET /solutions` (base URL `https://app.smartsuite.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-solutions.md) for the provider-specific parameters and requirements.

