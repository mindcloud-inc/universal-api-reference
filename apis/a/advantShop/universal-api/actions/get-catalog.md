# AdvantShop: Get Catalog

Retrieves the catalog from AdvantShop.

```
GET https://connect.mindcloud.co/v1/universal/advantShop/latest/actions/get-catalog
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AdvantShop `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/advantShop/latest/actions/get-catalog?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/advantShop/latest/actions/get-catalog?${params}`, {
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
| `categoryId` | number | no | Category ID. AdvantShop requires either categoryId or url for catalog requests. |
| `url` | string | no | Category URL. AdvantShop requires either categoryId or url for catalog requests. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "name": "Ava Chen",
      "products": [
        {}
      ],
      "productsCount": 1,
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `name` | string |  |
| `products` | array<object> |  |
| `productsCount` | number |  |
| `url` | string |  |

## Native endpoint

Through the native AdvantShop API, this operation is `POST /catalog` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-catalog.md) for the provider-specific parameters and requirements.

