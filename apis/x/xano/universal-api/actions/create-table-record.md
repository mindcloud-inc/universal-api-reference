# Xano: Create Table Record

Creates a new record in a Xano table.

```
POST https://connect.mindcloud.co/v1/universal/xano/latest/actions/create-table-record
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Xano `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/xano/latest/actions/create-table-record" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "table_id": 1,
  "workspace_id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/xano/latest/actions/create-table-record', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "table_id": 1,
    "workspace_id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `table_id` | number | yes |  |
| `workspace_id` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": 1,
      "id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | number |  |
| `id` | number |  |

## Native endpoint

Through the native Xano API, this operation is `POST /api%3Ameta/workspace/:workspace_id/table/:table_id/content` (base URL `https://x8ki-letl-twmt.n7.xano.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-table-record.md) for the provider-specific parameters and requirements.

