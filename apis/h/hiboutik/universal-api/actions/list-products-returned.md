# Hiboutik: List Products Returned

Retrieves returned products for a specific date in Hiboutik.

```
GET https://connect.mindcloud.co/v1/universal/hiboutik/latest/actions/list-products-returned
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hiboutik `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hiboutik/latest/actions/list-products-returned?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hiboutik/latest/actions/list-products-returned?${params}`, {
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
| `day` | string | no | The numeric day. |
| `month` | string | no | The numeric month. |
| `storeId` | string | no | The Hiboutik store id. |
| `year` | string | no | The four-digit year. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "productId": 1,
      "productModel": "string",
      "quantity": "string",
      "total": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `productId` | number |  |
| `productModel` | string |  |
| `quantity` | string |  |
| `total` | string |  |

## Native endpoint

Through the native Hiboutik API, this operation is `GET /products_returned/:store_id/:year/:month/:day` (base URL `https://mindcloudhiboutik20260402.hiboutik.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-products-returned.md) for the provider-specific parameters and requirements.

