# Umbrella: Update Integration

Updates an existing integration in Umbrella.

```
PUT https://connect.mindcloud.co/v1/universal/umbrella/latest/actions/update-integration
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Umbrella `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/umbrella/latest/actions/update-integration" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/umbrella/latest/actions/update-integration', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `intId` | string | no | The integration ID. |
| `name` | string | no | The updated integration name. |
| `webhookConfig.url` | string | no | The updated webhook destination URL. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "config": {},
      "createdAt": "2026-05-07T12:00:00.000Z",
      "createdBy": "string",
      "createdFromIp": "string",
      "href": "https://example.com",
      "id": "string",
      "name": "Ava Chen",
      "status": "string",
      "type": "string",
      "updatedFromIp": "string",
      "webhookConfig": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `config` | object |  |
| `createdAt` | date |  |
| `createdBy` | string |  |
| `createdFromIp` | string |  |
| `href` | string |  |
| `id` | string |  |
| `name` | string |  |
| `status` | string |  |
| `type` | string |  |
| `updatedFromIp` | string |  |
| `webhookConfig` | object |  |

## Native endpoint

Through the native Umbrella API, this operation is `PATCH https://api.sse.cisco.com/admin/v2/integrations/:intId` (base URL `https://api.umbrella.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-integration.md) for the provider-specific parameters and requirements.

