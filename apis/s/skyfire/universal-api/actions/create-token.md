# Skyfire: Create Token

Creates a new token in Skyfire.

```
POST https://connect.mindcloud.co/v1/universal/skyfire/latest/actions/create-token
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Skyfire `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/skyfire/latest/actions/create-token" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "type": "pay"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/skyfire/latest/actions/create-token', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "type": "pay"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `type` | string | yes | One of kya, pay, or kya-pay. Example: `pay`. |
| `buyerTag` | string | no | Buyer internal identifier for the transaction or token. Example: `invoice-123`. |
| `tokenAmount` | string | no | Amount for a pay or kya-pay token. Example: `0.01`. |
| `sellerServiceId` | string | no | One of either sellerServiceId or sellerDomainOrUrl is required. Example: `41779894-ece2-4163-9761-b3b1b76e19b0`. |
| `sellerDomainOrUrl` | string | no | One of either sellerServiceId or sellerDomainOrUrl is required. Example: `https://example.com/api`. |
| `expiresAt` | number | no | Seconds since the Unix epoch. Example: `1776966120`. |
| `identityPermissions[]` | array<string> | no | Additional identity fields to include in the token. Example: `given_name,family_name`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "token": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `token` | string |  |

## Native endpoint

Through the native Skyfire API, this operation is `POST /tokens` (base URL `https://api.skyfire.xyz/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-token.md) for the provider-specific parameters and requirements.

