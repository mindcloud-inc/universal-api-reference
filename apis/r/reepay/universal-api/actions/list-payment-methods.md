# Reepay: List Payment Methods

Retrieves payment methods from Reepay.

```
GET https://connect.mindcloud.co/v1/universal/reepay/latest/actions/list-payment-methods
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reepay `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/reepay/latest/actions/list-payment-methods?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/reepay/latest/actions/list-payment-methods?${params}`, {
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
      "created": "2026-05-07T12:00:00.000Z",
      "customer": "string",
      "id": "string",
      "offline_mandate": {
        "offline_agreement_handle": "string",
        "offline_agreement_name": "Ava Chen"
      },
      "payment_type": "string",
      "reference": "string",
      "state": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | date |  |
| `customer` | string |  |
| `id` | string |  |
| `offline_mandate.offline_agreement_handle` | string |  |
| `offline_mandate.offline_agreement_name` | string |  |
| `payment_type` | string |  |
| `reference` | string |  |
| `state` | string |  |

## Native endpoint

Through the native Reepay API, this operation is `GET /v1/list/payment_method` (base URL `https://api.frisbii.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-payment-methods.md) for the provider-specific parameters and requirements.

