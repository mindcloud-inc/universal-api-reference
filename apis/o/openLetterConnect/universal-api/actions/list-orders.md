# Open Letter Connect: List Orders

Retrieves orders from Open Letter Connect.

```
GET https://connect.mindcloud.co/v1/universal/openLetterConnect/latest/actions/list-orders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Open Letter Connect `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openLetterConnect/latest/actions/list-orders?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openLetterConnect/latest/actions/list-orders?${params}`, {
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
      "campaign": {
        "campaignType": "string",
        "deliveryDate": "string",
        "id": "string",
        "name": "Ava Chen",
        "scheduleType": "string"
      },
      "contacts": [
        {
          "contact": {
            "email": "ava@example.com",
            "fullName": "Ava Chen",
            "id": "string"
          },
          "id": "string",
          "isDelivered": true
        }
      ],
      "fileUrl": "https://example.com",
      "id": "string",
      "isLiveMode": true,
      "orgId": "string",
      "product": {
        "deliveryType": "string",
        "envelopeType": "string",
        "id": "string",
        "name": "Ava Chen",
        "paperSize": "string",
        "paperType": "string",
        "postageType": "string",
        "productType": "string"
      },
      "status": 1,
      "template": {
        "id": "string",
        "templateType": "string",
        "templateUrl": "https://example.com",
        "thumbnailUrl": "https://example.com",
        "title": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `campaign.campaignType` | string |  |
| `campaign.deliveryDate` | string |  |
| `campaign.id` | string |  |
| `campaign.name` | string |  |
| `campaign.scheduleType` | string |  |
| `contacts[].contact.email` | string |  |
| `contacts[].contact.fullName` | string |  |
| `contacts[].contact.id` | string |  |
| `contacts[].id` | string |  |
| `contacts[].isDelivered` | boolean |  |
| `fileUrl` | string |  |
| `id` | string |  |
| `isLiveMode` | boolean |  |
| `orgId` | string |  |
| `product.deliveryType` | string |  |
| `product.envelopeType` | string |  |
| `product.id` | string |  |
| `product.name` | string |  |
| `product.paperSize` | string |  |
| `product.paperType` | string |  |
| `product.postageType` | string |  |
| `product.productType` | string |  |
| `status` | number |  |
| `template.id` | string |  |
| `template.templateType` | string |  |
| `template.templateUrl` | string |  |
| `template.thumbnailUrl` | string |  |
| `template.title` | string |  |

## Native endpoint

Through the native Open Letter Connect API, this operation is `GET /orders` (base URL `https://api.openletterconnect.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-orders.md) for the provider-specific parameters and requirements.

