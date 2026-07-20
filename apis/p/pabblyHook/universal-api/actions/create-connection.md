# Pabbly Hook: Create Connection



```
POST https://connect.mindcloud.co/v1/universal/pabblyHook/latest/actions/create-connection
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pabbly Hook `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pabblyHook/latest/actions/create-connection" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Payment webhook",
  "folderId": "67592783069f7717b89ba992",
  "source": {},
  "destination": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pabblyHook/latest/actions/create-connection', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Payment webhook",
    "folderId": "67592783069f7717b89ba992",
    "source": {},
    "destination": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Connection name. Example: `Payment webhook`. |
| `folderId` | string | yes | Folder ID for the connection. Example: `67592783069f7717b89ba992`. |
| `source` | object | yes | Source configuration object. |
| `destination` | object | yes | Destination configuration object. |
| `retry` | object | no | Retry configuration object. |
| `delay` | object | no | Delay configuration object. |
| `transformationId` | string | no | Transformation ID to apply. Example: `trs_672cade8d3adcf3a0d314b1b`. |
| `filter` | object | no | Connection filter configuration object. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "connectionId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "delay": {},
      "destination": {},
      "disabledAt": "2026-05-07T12:00:00.000Z",
      "filter": {},
      "folderId": "string",
      "Id": "string",
      "name": "Ava Chen",
      "source": {},
      "status": "string",
      "transformation": {},
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "userId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `connectionId` | string | Public Pabbly Hook connection identifier. |
| `createdAt` | date | Creation timestamp. |
| `delay` | object | Delay configuration when enabled. |
| `destination` | object | Destination request configuration. |
| `disabledAt` | date | Timestamp when the connection was disabled, when present. |
| `filter` | object | Filter configuration when enabled. |
| `folderId` | string | Folder identifier containing the connection. |
| `Id` | string | Pabbly Hook internal connection identifier. |
| `name` | string | Connection name. |
| `source` | object | Webhook source configuration. |
| `status` | string | Connection status. |
| `transformation` | object | Transformation configuration when attached. |
| `updatedAt` | date | Last update timestamp. |
| `userId` | string | Pabbly account user identifier. |

## Native endpoint

Through the native Pabbly Hook API, this operation is `POST /api/v1/connections` (base URL `https://hook.pabbly.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-connection.md) for the provider-specific parameters and requirements.

