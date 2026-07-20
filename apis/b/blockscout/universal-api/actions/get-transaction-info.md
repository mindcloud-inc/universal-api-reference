# Blockscout: Get Transaction Info

Retrieves a transaction's details from Blockscout.

```
GET https://connect.mindcloud.co/v1/universal/blockscout/latest/actions/get-transaction-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Blockscout `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/blockscout/latest/actions/get-transaction-info?connectionId=$CONNECTION_ID&transaction_hash_param=0x9cf935b572365d677a8021c81ca23ee9d4d41b8dc637537f58827754fb127fa3" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "transaction_hash_param": "0x9cf935b572365d677a8021c81ca23ee9d4d41b8dc637537f58827754fb127fa3"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/blockscout/latest/actions/get-transaction-info?${params}`, {
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
| `chain_id` | string | no | Default: `10`. |
| `transaction_hash_param` | string | yes | Transaction hash to retrieve. Default: `0x9cf935b572365d677a8021c81ca23ee9d4d41b8dc637537f58827754fb127fa3`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "block_number": 1,
      "hash": "string",
      "method": "string",
      "status": "string",
      "timestamp": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `block_number` | number |  |
| `hash` | string |  |
| `method` | string |  |
| `status` | string |  |
| `timestamp` | date |  |

## Native endpoint

Through the native Blockscout API, this operation is `GET /:chain_id/api/v2/transactions/:transaction_hash_param` (base URL `https://api.blockscout.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-transaction-info.md) for the provider-specific parameters and requirements.

