# Blockscout: Get Smart Contracts

Retrieves verified smart contracts from Blockscout.

```
GET https://connect.mindcloud.co/v1/universal/blockscout/latest/actions/get-smart-contracts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Blockscout `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/blockscout/latest/actions/get-smart-contracts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/blockscout/latest/actions/get-smart-contracts?${params}`, {
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

Through the native Blockscout API, this operation is `GET /:chain_id/api/v2/smart-contracts/` (base URL `https://api.blockscout.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-smart-contracts.md) for the provider-specific parameters and requirements.

