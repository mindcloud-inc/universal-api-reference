# Svix: Patch Endpoint

Updates an endpoint in Svix.

```
PUT https://connect.mindcloud.co/v1/universal/svix/latest/actions/patch-endpoint
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Svix `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/svix/latest/actions/patch-endpoint" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "appId": "string",
  "endpointId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/svix/latest/actions/patch-endpoint', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "appId": "string",
    "endpointId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `appId` | string | yes | The application's ID or UID. |
| `endpointId` | string | yes | The endpoint's ID or UID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "channels": [
        "string"
      ],
      "createdAt": "string",
      "description": "string",
      "disabled": true,
      "filterTypes": [
        "string"
      ],
      "id": "string",
      "metadata": {},
      "rateLimit": 1,
      "throttleRate": 1,
      "uid": "string",
      "updatedAt": "string",
      "url": "https://example.com",
      "version": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `channels` | array<string> |  |
| `createdAt` | string |  |
| `description` | string |  |
| `disabled` | boolean |  |
| `filterTypes` | array<string> |  |
| `id` | string |  |
| `metadata` | object |  |
| `rateLimit` | number |  |
| `throttleRate` | number |  |
| `uid` | string |  |
| `updatedAt` | string |  |
| `url` | string |  |
| `version` | number |  |

## Native endpoint

Through the native Svix API, this operation is `PATCH /api/v1/app/{app_id}/endpoint/{endpoint_id}` (base URL `https://api.us.svix.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/patch-endpoint.md) for the provider-specific parameters and requirements.

