# Hightouch: Update Destination

Updates an existing destination in Hightouch.

```
PUT https://connect.mindcloud.co/v1/universal/hightouch/latest/actions/update-destination
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hightouch `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/hightouch/latest/actions/update-destination" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "destinationId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hightouch/latest/actions/update-destination', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "destinationId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `destinationId` | number | yes | The destination ID. |
| `name` | string | no | The destination name. |
| `configuration` | object | no | Destination configuration object for the selected destination type. |

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
      "syncs": [
        1
      ],
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
| `configuration` | object | Destination configuration. |
| `createdAt` | date | Creation timestamp. |
| `id` | number | Destination ID. |
| `name` | string | Destination name. |
| `slug` | string | Destination slug. |
| `syncs` | array<number> | Sync IDs using this destination. |
| `type` | string | Destination type. |
| `updatedAt` | date | Last update timestamp. |
| `workspaceId` | number | Workspace ID. |

## Native endpoint

Through the native Hightouch API, this operation is `PATCH /destinations/{destinationId}` (base URL `https://api.hightouch.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-destination.md) for the provider-specific parameters and requirements.

