# SmartSuite: Get Solution

Retrieves a solution from SmartSuite.

```
GET https://connect.mindcloud.co/v1/universal/smartSuite/latest/actions/get-solution
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SmartSuite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smartSuite/latest/actions/get-solution?connectionId=$CONNECTION_ID&solutionId=69b45da87cb40fc74dbb4b83" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "solutionId": "69b45da87cb40fc74dbb4b83"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smartSuite/latest/actions/get-solution?${params}`, {
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
| `solutionId` | string | yes | The SmartSuite solution ID to fetch. Example: `69b45da87cb40fc74dbb4b83`. |

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
                "textAlign": {}
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
| `description.data.content[].attrs.textAlign` | object |  |
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

Through the native SmartSuite API, this operation is `GET /solutions/:solutionId/` (base URL `https://app.smartsuite.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-solution.md) for the provider-specific parameters and requirements.

