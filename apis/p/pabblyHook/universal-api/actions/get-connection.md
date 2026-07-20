# Pabbly Hook: Get Connection



```
GET https://connect.mindcloud.co/v1/universal/pabblyHook/latest/actions/get-connection
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pabbly Hook `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pabblyHook/latest/actions/get-connection?connectionId=$CONNECTION_ID&connectionId=conn_ee3a07ef5a574f58abc4a2d98a5c2d3b" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "connectionId": "conn_ee3a07ef5a574f58abc4a2d98a5c2d3b"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pabblyHook/latest/actions/get-connection?${params}`, {
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
| `connectionId` | string | yes | Connection ID to retrieve. Example: `conn_ee3a07ef5a574f58abc4a2d98a5c2d3b`. |

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

Through the native Pabbly Hook API, this operation is `GET /api/v1/connections/:connectionId` (base URL `https://hook.pabbly.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-connection.md) for the provider-specific parameters and requirements.

