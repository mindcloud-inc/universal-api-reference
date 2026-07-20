# Fintoc: List Transfers

Retrieves transfers from Fintoc.

```
GET https://connect.mindcloud.co/v1/universal/fintoc/latest/actions/list-transfers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fintoc `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fintoc/latest/actions/list-transfers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fintoc/latest/actions/list-transfers?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "account_number": {},
      "amount": 1,
      "comment": "string",
      "counterparty": {},
      "currency": "string",
      "direction": "string",
      "id": "string",
      "metadata": {},
      "mode": "string",
      "object": "string",
      "post_date": "string",
      "receipt_url": "https://example.com",
      "reference_id": "string",
      "return_reason": "string",
      "status": "string",
      "tracking_key": "string",
      "transaction_date": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account_number` | object |  |
| `amount` | number |  |
| `comment` | string |  |
| `counterparty` | object |  |
| `currency` | string |  |
| `direction` | string |  |
| `id` | string |  |
| `metadata` | object |  |
| `mode` | string |  |
| `object` | string |  |
| `post_date` | string |  |
| `receipt_url` | string |  |
| `reference_id` | string |  |
| `return_reason` | string |  |
| `status` | string |  |
| `tracking_key` | string |  |
| `transaction_date` | string |  |

## Native endpoint

Through the native Fintoc API, this operation is `GET /v2/transfers` (base URL `https://api.fintoc.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-transfers.md) for the provider-specific parameters and requirements.

