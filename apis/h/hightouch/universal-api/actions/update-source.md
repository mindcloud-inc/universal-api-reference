# Hightouch: Update Source

Updates an existing source in Hightouch.

```
PUT https://connect.mindcloud.co/v1/universal/hightouch/latest/actions/update-source
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hightouch `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/hightouch/latest/actions/update-source" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "sourceId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hightouch/latest/actions/update-source', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "sourceId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | no | The source name. |
| `sourceId` | number | yes | The source ID. |
| `configuration` | object | no | Source configuration object for the selected source type. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "configuration": {},
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "name": "Ava Chen",
      "slug": "string",
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "workspaceId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `configuration` | object | Source configuration. |
| `createdAt` | date | Creation timestamp. |
| `id` | number | Source ID. |
| `name` | string | Source name. |
| `slug` | string | Source slug. |
| `type` | string | Source type. |
| `updatedAt` | date | Last update timestamp. |
| `workspaceId` | number | Workspace ID. |

## Native endpoint

Through the native Hightouch API, this operation is `PATCH /sources/{sourceId}` (base URL `https://api.hightouch.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-source.md) for the provider-specific parameters and requirements.

