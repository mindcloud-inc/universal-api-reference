# Bika.ai: List Space Nodes

Retrieves nodes from a Bika.ai space.

```
GET https://connect.mindcloud.co/v1/universal/bikaai/latest/actions/list-space-nodes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bika.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bikaai/latest/actions/list-space-nodes?connectionId=$CONNECTION_ID&spaceId=spcfaZbYtV5hkHSLrDOqY4ve" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "spaceId": "spcfaZbYtV5hkHSLrDOqY4ve"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bikaai/latest/actions/list-space-nodes?${params}`, {
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
| `spaceId` | string | yes | Bika.ai space ID. Example: `spcfaZbYtV5hkHSLrDOqY4ve`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "data": [
        {
          "description": "string",
          "hasPermissions": true,
          "hasShareLock": true,
          "id": "string",
          "name": "Ava Chen",
          "parentId": "string",
          "permission": {},
          "preNodeId": "string",
          "scope": "string",
          "sharing": true,
          "statusBadge": [
            {}
          ],
          "type": "string"
        }
      ],
      "message": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number |  |
| `data` | array<object> |  |
| `data[].description` | string |  |
| `data[].hasPermissions` | boolean |  |
| `data[].hasShareLock` | boolean |  |
| `data[].id` | string |  |
| `data[].name` | string |  |
| `data[].parentId` | string |  |
| `data[].permission` | object |  |
| `data[].preNodeId` | string |  |
| `data[].scope` | string |  |
| `data[].sharing` | boolean |  |
| `data[].statusBadge` | array<object> |  |
| `data[].type` | string |  |
| `message` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Bika.ai API, this operation is `GET /spaces/:spaceId/nodes` (base URL `https://bika.ai/api/openapi/bika/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-space-nodes.md) for the provider-specific parameters and requirements.

