# Open Letter Connect: Get Order

Retrieves an order from Open Letter Connect.

```
GET https://connect.mindcloud.co/v1/universal/openLetterConnect/latest/actions/get-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Open Letter Connect `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openLetterConnect/latest/actions/get-order?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openLetterConnect/latest/actions/get-order?${params}`, {
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
| `id` | number | yes | The numeric order ID from Open Letter Connect. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "backTemplateUrl": "https://example.com",
      "campaign": {
        "deliveryDate": "string",
        "scheduleType": "string"
      },
      "createdBy": "string",
      "creator": {
        "fullName": "Ava Chen",
        "id": "string"
      },
      "id": "string",
      "isLiveMode": true,
      "orgId": "string",
      "product": {
        "productType": "string"
      },
      "source": "string",
      "status": "string",
      "templateUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `backTemplateUrl` | string |  |
| `campaign.deliveryDate` | string |  |
| `campaign.scheduleType` | string |  |
| `createdBy` | string |  |
| `creator.fullName` | string |  |
| `creator.id` | string |  |
| `id` | string |  |
| `isLiveMode` | boolean |  |
| `orgId` | string |  |
| `product.productType` | string |  |
| `source` | string |  |
| `status` | string |  |
| `templateUrl` | string |  |

## Native endpoint

Through the native Open Letter Connect API, this operation is `GET /orders/:id` (base URL `https://api.openletterconnect.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-order.md) for the provider-specific parameters and requirements.

