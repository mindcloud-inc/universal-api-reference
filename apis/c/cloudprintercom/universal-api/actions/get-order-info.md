# Cloudprinter.com: Get Order Info

Retrieves order details from Cloudprinter.com.

```
GET https://connect.mindcloud.co/v1/universal/cloudprintercom/latest/actions/get-order-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloudprinter.com `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloudprintercom/latest/actions/get-order-info?connectionId=$CONNECTION_ID&reference=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "reference": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloudprintercom/latest/actions/get-order-info?${params}`, {
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
| `reference` | string | yes | Client order reference. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "addresses": [
        [
          {}
        ]
      ],
      "email": "ava@example.com",
      "is_cancelable": true,
      "items": [
        [
          {}
        ]
      ],
      "order_date": "string",
      "reference": "string",
      "state": 1,
      "state_code": "string",
      "status_logs": [
        [
          {}
        ]
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `addresses[]` | array<object> |  |
| `addresses[].city` | string |  |
| `addresses[].country` | string |  |
| `addresses[].email` | string |  |
| `addresses[].firstname` | string |  |
| `addresses[].lastname` | string |  |
| `addresses[].phone` | string |  |
| `addresses[].state` | string |  |
| `addresses[].street1` | string |  |
| `addresses[].type` | string |  |
| `addresses[].zip` | string |  |
| `email` | string |  |
| `is_cancelable` | boolean |  |
| `items[]` | array<object> |  |
| `items[].count` | number |  |
| `items[].files[]` | array<object> |  |
| `items[].files[].format` | string |  |
| `items[].files[].md5sum` | string |  |
| `items[].files[].type` | string |  |
| `items[].files[].url` | string |  |
| `items[].is_reordable` | boolean |  |
| `items[].name` | string |  |
| `items[].options[]` | array<object> |  |
| `items[].product_reference` | string |  |
| `items[].reference` | string |  |
| `items[].shipping_option` | string |  |
| `items[].shipping_option_reference` | string |  |
| `items[].state` | number |  |
| `items[].state_code` | string |  |
| `items[].title` | string |  |
| `items[].type` | string |  |
| `order_date` | string |  |
| `reference` | string |  |
| `state` | number |  |
| `state_code` | string |  |
| `status_logs[]` | array<object> |  |
| `status_logs[].create_date` | string |  |
| `status_logs[].reference` | string |  |
| `status_logs[].state` | number |  |

## Native endpoint

Through the native Cloudprinter.com API, this operation is `POST /cloudcore/1.0/orders/info` (base URL `https://api.cloudprinter.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-order-info.md) for the provider-specific parameters and requirements.

