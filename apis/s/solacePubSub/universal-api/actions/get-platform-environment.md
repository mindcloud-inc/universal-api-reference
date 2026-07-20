# Solace PubSub+: Get Platform Environment

Retrieves a platform environment from Solace PubSub+.

```
GET https://connect.mindcloud.co/v1/universal/solacePubSub/latest/actions/get-platform-environment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Solace PubSub+ `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/solacePubSub/latest/actions/get-platform-environment?connectionId=$CONNECTION_ID&id=bv8dag6sk7v" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "bv8dag6sk7v"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/solacePubSub/latest/actions/get-platform-environment?${params}`, {
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
| `id` | string | yes | Environment identifier. Default: `bv8dag6sk7v`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdTime": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "id": "string",
      "isDefault": true,
      "isProduction": true,
      "name": "Ava Chen",
      "organization": {},
      "type": "string",
      "updatedTime": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdTime` | date |  |
| `description` | string |  |
| `id` | string |  |
| `isDefault` | boolean |  |
| `isProduction` | boolean |  |
| `name` | string |  |
| `organization` | object |  |
| `type` | string |  |
| `updatedTime` | date |  |

## Native endpoint

Through the native Solace PubSub+ API, this operation is `GET /api/v2/platform/environments/{id}` (base URL `https://api.solace.cloud`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-platform-environment.md) for the provider-specific parameters and requirements.

