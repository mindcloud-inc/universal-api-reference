# SmartSuite: List Comments

Retrieves comments from SmartSuite.

```
GET https://connect.mindcloud.co/v1/universal/smartSuite/latest/actions/list-comments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SmartSuite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smartSuite/latest/actions/list-comments?connectionId=$CONNECTION_ID&recordId=69b45da87cb40fc74dbb4b8c" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "recordId": "69b45da87cb40fc74dbb4b8c"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smartSuite/latest/actions/list-comments?${params}`, {
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
| `recordId` | string | yes | The SmartSuite record ID to list comments for. Example: `69b45da87cb40fc74dbb4b8c`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `tableId` | string | no | Optional SmartSuite table ID filter. Example: `69b45da87cb40fc74dbb4b84`. |
| `solutionId` | string | no | Optional SmartSuite solution ID filter. Example: `69b45da87cb40fc74dbb4b83`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": {},
      "next": {},
      "previous": {},
      "results": [
        {
          "application": "string",
          "assignedTo": {},
          "createdOn": "string",
          "deletedOn": {},
          "email": {},
          "fieldSlug": {},
          "followers": [
            "string"
          ],
          "id": "string",
          "key": 1,
          "member": "string",
          "message": {
            "data": {
              "content": [
                {
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
          "parentComment": {},
          "record": "string",
          "resolvedBy": {},
          "solution": "string",
          "type": "string",
          "updatedOn": {}
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | object |  |
| `next` | object |  |
| `previous` | object |  |
| `results[].application` | string |  |
| `results[].assignedTo` | object |  |
| `results[].createdOn` | string |  |
| `results[].deletedOn` | object |  |
| `results[].email` | object |  |
| `results[].fieldSlug` | object |  |
| `results[].followers[]` | string |  |
| `results[].id` | string |  |
| `results[].key` | number |  |
| `results[].member` | string |  |
| `results[].message.data.content[].content[].text` | string |  |
| `results[].message.data.content[].content[].type` | string |  |
| `results[].message.data.content[].type` | string |  |
| `results[].message.data.type` | string |  |
| `results[].message.html` | string |  |
| `results[].message.preview` | string |  |
| `results[].parentComment` | object |  |
| `results[].record` | string |  |
| `results[].resolvedBy` | object |  |
| `results[].solution` | string |  |
| `results[].type` | string |  |
| `results[].updatedOn` | object |  |

## Native endpoint

Through the native SmartSuite API, this operation is `GET /comments/` (base URL `https://app.smartsuite.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-comments.md) for the provider-specific parameters and requirements.

