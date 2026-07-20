# STEL Order: List Payment Options

Retrieves a list of payment options from STEL Order.

```
GET https://connect.mindcloud.co/v1/universal/sTELOrder/latest/actions/list-payment-options
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a STEL Order `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sTELOrder/latest/actions/list-payment-options?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sTELOrder/latest/actions/list-payment-options?${params}`, {
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
      "default": true,
      "deleted": true,
      "description": "string",
      "id": 1,
      "linked-to-bank-account": true,
      "mxn-cfdi-key": "string",
      "name": "Ava Chen",
      "path": "string",
      "subject-to-sepa-payment": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `default` | boolean |  |
| `deleted` | boolean |  |
| `description` | string |  |
| `id` | number |  |
| `linked-to-bank-account` | boolean |  |
| `mxn-cfdi-key` | string |  |
| `name` | string |  |
| `path` | string |  |
| `subject-to-sepa-payment` | boolean |  |

## Native endpoint

Through the native STEL Order API, this operation is `GET /paymentOptions` (base URL `https://app.stelorder.com/app`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-payment-options.md) for the provider-specific parameters and requirements.

