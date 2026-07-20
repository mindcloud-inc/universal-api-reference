# G2: Get Vendor

Retrieves a vendor from G2.

```
GET https://connect.mindcloud.co/v1/universal/g2/latest/actions/get-vendor
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a G2 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/g2/latest/actions/get-vendor?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/g2/latest/actions/get-vendor?${params}`, {
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
| `id` | string | yes | Vendor UUID or slug from the G2 API spec. |

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

Through the native G2 API, this operation is `GET /api/v2/vendors/:id` (base URL `https://data.g2.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-vendor.md) for the provider-specific parameters and requirements.

