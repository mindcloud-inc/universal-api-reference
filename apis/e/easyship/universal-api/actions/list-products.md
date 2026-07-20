# Easyship: List Products

Retrieves a list of products from Easyship.

```
GET https://connect.mindcloud.co/v1/universal/easyship/latest/actions/list-products
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Easyship `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/easyship/latest/actions/list-products?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/easyship/latest/actions/list-products?${params}`, {
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
      "comments": "string",
      "containsBatteryPi966": true,
      "containsBatteryPi967": true,
      "containsLiquids": true,
      "createdAt": "string",
      "height": 1,
      "hsCode": "string",
      "id": "string",
      "identifier": "string",
      "imageUrl": "https://example.com",
      "inputType": "string",
      "itemCategory": {
        "id": 1,
        "name": "Ava Chen"
      },
      "length": 1,
      "name": "Ava Chen",
      "originCountryAlpha2": "string",
      "pickLocation": "string",
      "updatedAt": "string",
      "weight": 1,
      "width": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `comments` | string |  |
| `containsBatteryPi966` | boolean |  |
| `containsBatteryPi967` | boolean |  |
| `containsLiquids` | boolean |  |
| `createdAt` | string |  |
| `height` | number |  |
| `hsCode` | string |  |
| `id` | string |  |
| `identifier` | string |  |
| `imageUrl` | string |  |
| `inputType` | string |  |
| `itemCategory` | object |  |
| `itemCategory.id` | number |  |
| `itemCategory.name` | string |  |
| `length` | number |  |
| `name` | string |  |
| `originCountryAlpha2` | string |  |
| `pickLocation` | string |  |
| `updatedAt` | string |  |
| `weight` | number |  |
| `width` | number |  |

## Native endpoint

Through the native Easyship API, this operation is `GET /products` (base URL `https://public-api.easyship.com/2024-09`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-products.md) for the provider-specific parameters and requirements.

