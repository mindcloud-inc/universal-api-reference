# Dremio: Get External Token Provider

Retrieves an external token provider from Dremio by ID.

```
GET https://connect.mindcloud.co/v1/universal/dremio/latest/actions/get-external-token-provider
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dremio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dremio/latest/actions/get-external-token-provider?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dremio/latest/actions/get-external-token-provider?${params}`, {
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
| `id` | string | yes |  |

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

Through the native Dremio API, this operation is `GET /external-token-providers/:id` (base URL `https://api.dremio.cloud/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-external-token-provider.md) for the provider-specific parameters and requirements.

