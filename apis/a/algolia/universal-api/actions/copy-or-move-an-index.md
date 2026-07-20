# Algolia: Copy or Move an Index

Copies or moves an Algolia index.

```
PUT https://connect.mindcloud.co/v1/universal/algolia/latest/actions/copy-or-move-an-index
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Algolia `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/algolia/latest/actions/copy-or-move-an-index" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "indexName": "Ava Chen",
  "operation": "copy",
  "destination": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/algolia/latest/actions/copy-or-move-an-index', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "indexName": "Ava Chen",
    "operation": "copy",
    "destination": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `indexName` | string | yes | The source Algolia index. |
| `operation` | list | yes | Whether to copy or move the index. One of: `0`, `1`. Default: `copy`. |
| `destination` | string | yes | Destination index name. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `scope[]` | array<string> | no | Scopes to copy when using the copy operation. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "taskID": 1,
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `taskID` | number |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Algolia API, this operation is `POST /1/indexes/:indexName/operation` (base URL `https://{{credentials.applicationId}}.algolia.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/copy-or-move-an-index.md) for the provider-specific parameters and requirements.

