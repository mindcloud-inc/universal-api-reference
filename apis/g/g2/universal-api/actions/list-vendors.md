# G2: List Vendors

Retrieves vendors from G2.

```
GET https://connect.mindcloud.co/v1/universal/g2/latest/actions/list-vendors
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a G2 `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/g2/latest/actions/list-vendors?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/g2/latest/actions/list-vendors?${params}`, {
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
      "attributes": {
        "companyWebsite": "string",
        "description": "string",
        "name": "Ava Chen",
        "publicProductsCount": 1,
        "slug": "string",
        "updatedAt": "string"
      },
      "id": "string",
      "relationships": {
        "products": {
          "data": [
            {
              "id": "string",
              "type": "string"
            }
          ]
        }
      },
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes.companyWebsite` | string |  |
| `attributes.description` | string |  |
| `attributes.name` | string |  |
| `attributes.publicProductsCount` | number |  |
| `attributes.slug` | string |  |
| `attributes.updatedAt` | string |  |
| `id` | string |  |
| `relationships.products.data[].id` | string |  |
| `relationships.products.data[].type` | string |  |
| `type` | string |  |

## Native endpoint

Through the native G2 API, this operation is `GET /api/v2/vendors` (base URL `https://data.g2.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-vendors.md) for the provider-specific parameters and requirements.

