# Dremio: Update External Token Provider

Updates an external token provider in Dremio.

```
PUT https://connect.mindcloud.co/v1/universal/dremio/latest/actions/update-external-token-provider
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dremio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/dremio/latest/actions/update-external-token-provider" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "provider": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dremio/latest/actions/update-external-token-provider', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "provider": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes |  |
| `provider` | object | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "audience": [
        "string"
      ],
      "id": "string",
      "isActive": true,
      "issuerUrl": "https://example.com",
      "jwksUrl": "https://example.com",
      "name": "Ava Chen",
      "userClaim": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `audience` | array<string> |  |
| `id` | string |  |
| `isActive` | boolean |  |
| `issuerUrl` | string |  |
| `jwksUrl` | string |  |
| `name` | string |  |
| `userClaim` | string |  |

## Native endpoint

Through the native Dremio API, this operation is `PUT /external-token-providers/:id` (base URL `https://api.dremio.cloud/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-external-token-provider.md) for the provider-specific parameters and requirements.

