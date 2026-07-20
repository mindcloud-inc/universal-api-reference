# ActivityInfo: Get Database Tree

Retrieves a database tree from ActivityInfo.

```
GET https://connect.mindcloud.co/v1/universal/activityInfo/latest/actions/get-database-tree
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ActivityInfo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/activityInfo/latest/actions/get-database-tree?connectionId=$CONNECTION_ID&databaseId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "databaseId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/activityInfo/latest/actions/get-database-tree?${params}`, {
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
| `databaseId` | string | yes | ActivityInfo database ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "databaseId": "string",
      "description": "string",
      "grants": [
        {}
      ],
      "label": "string",
      "ownerRef": {},
      "resources": [
        {}
      ],
      "roles": [
        {}
      ],
      "userId": "string",
      "version": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `databaseId` | string | Database ID. |
| `description` | string | Database description. |
| `grants` | array<object> | Permission grants. |
| `label` | string | Database label. |
| `ownerRef` | object | Owner reference. |
| `resources` | array<object> | Folders, forms, reports, and subforms. |
| `roles` | array<object> | Database roles. |
| `userId` | string | Requesting user ID. |
| `version` | string | Database tree version. |

## Native endpoint

Through the native ActivityInfo API, this operation is `GET /resources/databases/:databaseId` (base URL `https://www.activityinfo.org`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-database-tree.md) for the provider-specific parameters and requirements.

