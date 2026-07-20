# Hightouch: Create Destination

Creates a new destination in Hightouch.

```
POST https://connect.mindcloud.co/v1/universal/hightouch/latest/actions/create-destination
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hightouch `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/hightouch/latest/actions/create-destination" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "slug": "string",
  "type": "string",
  "configuration": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hightouch/latest/actions/create-destination', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "slug": "string",
    "type": "string",
    "configuration": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | The destination name. |
| `slug` | string | yes | The destination slug. |
| `type` | string | yes | The destination type, such as salesforce or hubspot. |
| `configuration` | object | yes | Destination configuration object for the selected destination type. |

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

Through the native Hightouch API, this operation is `POST /destinations` (base URL `https://api.hightouch.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-destination.md) for the provider-specific parameters and requirements.

