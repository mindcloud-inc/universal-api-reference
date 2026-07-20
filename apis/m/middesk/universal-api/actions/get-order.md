# Middesk: Retrieve an order

Retrieves an order from your Middesk account.

```
GET https://connect.mindcloud.co/v1/universal/middesk/latest/actions/get-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Middesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/middesk/latest/actions/get-order?connectionId=$CONNECTION_ID&businessId=string&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "businessId": "string",
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/middesk/latest/actions/get-order?${params}`, {
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
| `businessId` | string | yes | ID of the business that owns the order. |
| `id` | string | yes | ID of the order to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "businessId": "string",
      "completedAt": "string",
      "createdAt": "string",
      "id": "string",
      "monitoring": true,
      "object": "string",
      "package": "string",
      "product": "string",
      "requester": {},
      "status": "string",
      "subproducts": [
        "string"
      ],
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `businessId` | string |  |
| `completedAt` | string |  |
| `createdAt` | string |  |
| `id` | string |  |
| `monitoring` | boolean |  |
| `object` | string |  |
| `package` | string |  |
| `product` | string |  |
| `requester` | object |  |
| `status` | string |  |
| `subproducts` | array<string> |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Middesk API, this operation is `GET /businesses/:business_id/orders/:id` (base URL `https://api.middesk.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-order.md) for the provider-specific parameters and requirements.

