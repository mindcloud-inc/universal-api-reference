# KEYZY: List Register Products

Checks serial eligibility and previews registered products in KEYZY.

```
GET https://connect.mindcloud.co/v1/universal/kEYZY/latest/actions/list-register-products
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a KEYZY `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kEYZY/latest/actions/list-register-products?connectionId=$CONNECTION_ID&serial=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "serial": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kEYZY/latest/actions/list-register-products?${params}`, {
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
| `serial` | string | yes | A license serial number. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "createdAt": "string",
          "dealerId": 1,
          "dealerName": "Ava Chen",
          "email": "ava@example.com",
          "endAt": 1,
          "id": 1,
          "imageUrl": "https://example.com",
          "name": "Ava Chen",
          "registered": true,
          "serial": "string",
          "skuId": 1,
          "skuName": "Ava Chen",
          "skuNumber": "string",
          "skuUrl": "https://example.com",
          "startAt": 1,
          "type": "string",
          "updatedAt": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[].createdAt` | string | Creation timestamp. |
| `data[].dealerId` | number | Dealer ID. |
| `data[].dealerName` | string | Dealer name. |
| `data[].email` | string | Registered user email. |
| `data[].endAt` | number | License end timestamp. |
| `data[].id` | number | Registered product row ID. |
| `data[].imageUrl` | string | Image URL. |
| `data[].name` | string | Registered user name. |
| `data[].registered` | boolean | Whether the product is registered. |
| `data[].serial` | string | License serial number. |
| `data[].skuId` | number | SKU ID. |
| `data[].skuName` | string | SKU name. |
| `data[].skuNumber` | string | SKU number. |
| `data[].skuUrl` | string | SKU URL. |
| `data[].startAt` | number | License start timestamp. |
| `data[].type` | string | License type. |
| `data[].updatedAt` | string | Last update timestamp. |

## Native endpoint

Through the native KEYZY API, this operation is `GET /register-products/:serial` (base URL `https://api.keyzy.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-register-products.md) for the provider-specific parameters and requirements.

