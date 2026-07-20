# Dremio: Update Identity Provider

Updates an identity provider in Dremio.

```
PUT https://connect.mindcloud.co/v1/universal/dremio/latest/actions/update-identity-provider
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dremio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/dremio/latest/actions/update-identity-provider" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "provider": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dremio/latest/actions/update-identity-provider', {
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
      "clientID": "string",
      "clientSecret": "string",
      "domain": "string",
      "id": "string",
      "isActive": true,
      "issuerUrl": "https://example.com",
      "oktaUrl": "https://example.com",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `clientID` | string |  |
| `clientSecret` | string |  |
| `domain` | string |  |
| `id` | string |  |
| `isActive` | boolean |  |
| `issuerUrl` | string |  |
| `oktaUrl` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Dremio API, this operation is `PUT /identity-providers/:id` (base URL `https://api.dremio.cloud/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-identity-provider.md) for the provider-specific parameters and requirements.

