# Blockscout: Get Token Transfers by Token

Retrieves transfers for a token from Blockscout.

```
GET https://connect.mindcloud.co/v1/universal/blockscout/latest/actions/get-token-transfers-by-token
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Blockscout `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/blockscout/latest/actions/get-token-transfers-by-token?connectionId=$CONNECTION_ID&address_hash_param=0x0b2C639c533813f4Aa9D7837CAf62653d097Ff85" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "address_hash_param": "0x0b2C639c533813f4Aa9D7837CAf62653d097Ff85"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/blockscout/latest/actions/get-token-transfers-by-token?${params}`, {
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
| `chain_id` | string | no | Blockscout chain ID, for example 10 for Optimism. Default: `10`. |
| `address_hash_param` | string | yes | Token contract address. Default: `0x0b2C639c533813f4Aa9D7837CAf62653d097Ff85`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "items": [
        {}
      ],
      "next_page_params": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `items` | array<object> |  |
| `next_page_params` | object |  |

## Native endpoint

Through the native Blockscout API, this operation is `GET /:chain_id/api/v2/tokens/:address_hash_param/transfers` (base URL `https://api.blockscout.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-token-transfers-by-token.md) for the provider-specific parameters and requirements.

