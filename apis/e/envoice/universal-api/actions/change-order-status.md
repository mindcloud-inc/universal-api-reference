# Envoice: Change Order Status

Updates an order status in Envoice.

```
PUT https://connect.mindcloud.co/v1/universal/envoice/latest/actions/change-order-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Envoice `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/envoice/latest/actions/change-order-status" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1,
  "status": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/envoice/latest/actions/change-order-status', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1,
    "status": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | Order identifier. |
| `reason` | string | no | Reason for status change. |
| `status` | string | yes | New order status. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ErrorMessages": [
        "string"
      ],
      "IsFaulted": true,
      "Success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ErrorMessages` | array<string> | Error messages returned by Envoice. |
| `IsFaulted` | boolean | Whether the request failed. |
| `Success` | boolean | Whether the order status was changed successfully. |

## Native endpoint

Through the native Envoice API, this operation is `POST order/changestatus` (base URL `https://www.envoice.in/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/change-order-status.md) for the provider-specific parameters and requirements.

