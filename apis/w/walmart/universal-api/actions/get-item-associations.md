# Walmart: Get Item Associations

Retrieve Shipping Templates and Fulfillment Centers associated with your item SKUs.

```
GET https://connect.mindcloud.co/v1/universal/walmart/latest/actions/get-item-associations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Walmart `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/walmart/latest/actions/get-item-associations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/walmart/latest/actions/get-item-associations?${params}`, {
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
| `items[]` | array<object> | no | List of items whose associations need to be fetched. The list should not exceed 50 items per request. |
| `items[].sku` | string | no | An arbitrary alphanumeric unique ID, specified by the seller, which identifies each item. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "associations": [
        {
          "shipNode": "string",
          "shipNodeName": "Ava Chen",
          "shippingTemplate": {
            "id": "string",
            "name": "Ava Chen",
            "type": "string"
          }
        }
      ],
      "sku": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `associations[].shipNode` | string |  |
| `associations[].shipNodeName` | string |  |
| `associations[].shippingTemplate.id` | string |  |
| `associations[].shippingTemplate.name` | string |  |
| `associations[].shippingTemplate.type` | string |  |
| `sku` | string |  |

## Native endpoint

Through the native Walmart API, this operation is `POST /v3/items/associations` (base URL `https://{{credentials.environment}}.walmartapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-item-associations.md) for the provider-specific parameters and requirements.

