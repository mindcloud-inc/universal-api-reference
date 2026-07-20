# Dremio: Create Identity Provider

Creates a new identity provider in Dremio.

```
POST https://connect.mindcloud.co/v1/universal/dremio/latest/actions/create-identity-provider
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dremio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dremio/latest/actions/create-identity-provider" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "providerPayload": {},
  "type": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dremio/latest/actions/create-identity-provider', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "providerPayload": {},
    "type": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `providerPayload` | object | yes |  |
| `type` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |

## Native endpoint

Through the native Dremio API, this operation is `POST /identity-providers` (base URL `https://api.dremio.cloud/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-identity-provider.md) for the provider-specific parameters and requirements.

