# Corporate Merch: Get Catalog By Id

Retrieves a catalog product from Corporate Merch.

```
GET https://connect.mindcloud.co/v1/universal/corporateMerch/latest/actions/get-catalog-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Corporate Merch `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/corporateMerch/latest/actions/get-catalog-by-id?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/corporateMerch/latest/actions/get-catalog-by-id?${params}`, {
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
      "estimatedShipDate": "string",
      "id": "string",
      "name": "Ava Chen",
      "quantity": 1,
      "unitPrice": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `estimatedShipDate` | string |  |
| `id` | string |  |
| `name` | string |  |
| `quantity` | number |  |
| `unitPrice` | string |  |

## Native endpoint

Through the native Corporate Merch API, this operation is `GET /v2/catalog/{id}` (base URL `https://api.corporatemerch.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-catalog-by-id.md) for the provider-specific parameters and requirements.

