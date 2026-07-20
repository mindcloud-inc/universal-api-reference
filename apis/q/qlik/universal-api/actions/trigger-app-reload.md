# Qlik: Trigger App Reload

Triggers an app reload in Qlik.

```
POST https://connect.mindcloud.co/v1/universal/qlik/latest/actions/trigger-app-reload
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Qlik `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/qlik/latest/actions/trigger-app-reload" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "appId": "65b8f2a1f4b0c2d3e4f56789"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/qlik/latest/actions/trigger-app-reload', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "appId": "65b8f2a1f4b0c2d3e4f56789"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `appId` | string | yes | Qlik app ID to reload. Example: `65b8f2a1f4b0c2d3e4f56789`. |
| `partial` | boolean | no | Whether to perform a partial reload. Example: `false`. |
| `variables` | object | no | Reload variables object. Example: `[object Object]`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "appId": "string",
      "endTime": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "status": "string",
      "tenantId": "string",
      "type": "string",
      "userId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `appId` | string |  |
| `endTime` | date |  |
| `id` | string |  |
| `status` | string |  |
| `tenantId` | string |  |
| `type` | string |  |
| `userId` | string |  |

## Native endpoint

Through the native Qlik API, this operation is `POST /api/v1/reloads` (base URL `https://{{credentials.tenantHost}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/trigger-app-reload.md) for the provider-specific parameters and requirements.

