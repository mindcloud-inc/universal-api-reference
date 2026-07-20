# Umbrella: Get Integration

Retrieves integration details from your Umbrella organization.

```
GET https://connect.mindcloud.co/v1/universal/umbrella/latest/actions/get-integration
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Umbrella `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/umbrella/latest/actions/get-integration?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/umbrella/latest/actions/get-integration?${params}`, {
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
| `intId` | string | no | The integration ID. |

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

Through the native Umbrella API, this operation is `GET https://api.sse.cisco.com/admin/v2/integrations/:intId` (base URL `https://api.umbrella.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-integration.md) for the provider-specific parameters and requirements.

