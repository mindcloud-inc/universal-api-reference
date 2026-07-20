# Privy: List Wallets

Retrieves a list of wallets from Privy.

```
GET https://connect.mindcloud.co/v1/universal/privy/latest/actions/list-wallets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Privy `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/privy/latest/actions/list-wallets?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/privy/latest/actions/list-wallets?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `chainType` | string | no | Optional wallet chain type filter. |
| `userId` | string | no | Optional user ID filter. |
| `authorizationKey` | string | no | Optional authorization key filter. |
| `externalId` | string | no | Optional external ID filter. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "address": "string",
          "chain_type": "string",
          "created_at": 1,
          "display_name": "Ava Chen",
          "external_id": "string",
          "id": "string",
          "policy_ids": [
            "string"
          ],
          "public_key": "string"
        }
      ],
      "next_cursor": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[].address` | string |  |
| `data[].chain_type` | string |  |
| `data[].created_at` | number |  |
| `data[].display_name` | string |  |
| `data[].external_id` | string |  |
| `data[].id` | string |  |
| `data[].policy_ids` | array<string> |  |
| `data[].public_key` | string |  |
| `next_cursor` | string |  |

## Native endpoint

Through the native Privy API, this operation is `GET /v1/wallets` (base URL `https://api.privy.io`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-wallets.md) for the provider-specific parameters and requirements.

