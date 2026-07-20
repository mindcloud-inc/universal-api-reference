# MoySklad: Delete customer order

Deletes a customer order from MoySklad.

```
DELETE https://connect.mindcloud.co/v1/universal/moySklad/latest/actions/delete-customer-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MoySklad `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/moySklad/latest/actions/delete-customer-order?connectionId=$CONNECTION_ID&id=28e45ad1-3d81-11f1-0a80-0b450021d671" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "28e45ad1-3d81-11f1-0a80-0b450021d671"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/moySklad/latest/actions/delete-customer-order?${params}`, {
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
| `id` | string | yes | MoySklad customer order ID. Default: `28e45ad1-3d81-11f1-0a80-0b450021d671`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "meta": {},
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `meta` | object |  |
| `success` | boolean |  |

## Native endpoint

Through the native MoySklad API, this operation is `DELETE entity/customerorder/:id` (base URL `https://api.moysklad.ru/api/remap/1.2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-customer-order.md) for the provider-specific parameters and requirements.

