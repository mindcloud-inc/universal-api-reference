# Unkey: Create Identity

Creates a new identity in Unkey.

```
POST https://connect.mindcloud.co/v1/universal/unkey/latest/actions/create-identity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Unkey `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/unkey/latest/actions/create-identity" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "externalId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/unkey/latest/actions/create-identity', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "externalId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `externalId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "identityId": "string"
      },
      "meta": {
        "requestId": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |
| `data.identityId` | string |  |
| `meta` | object |  |
| `meta.requestId` | string |  |

## Native endpoint

Through the native Unkey API, this operation is `POST /v2/identities.createIdentity` (base URL `https://api.unkey.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-identity.md) for the provider-specific parameters and requirements.

