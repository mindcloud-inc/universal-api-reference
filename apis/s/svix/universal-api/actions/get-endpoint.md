# Svix: Get Endpoint

Retrieves an endpoint from Svix.

```
GET https://connect.mindcloud.co/v1/universal/svix/latest/actions/get-endpoint
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Svix `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/svix/latest/actions/get-endpoint?connectionId=$CONNECTION_ID&appId=string&endpointId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "appId": "string",
  "endpointId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/svix/latest/actions/get-endpoint?${params}`, {
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

Through the native Svix API, this operation is `GET /api/v1/app/{app_id}/endpoint/{endpoint_id}` (base URL `https://api.us.svix.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-endpoint.md) for the provider-specific parameters and requirements.

