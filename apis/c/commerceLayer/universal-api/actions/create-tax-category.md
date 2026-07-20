# Commerce Layer: Create Tax Category



```
POST https://connect.mindcloud.co/v1/universal/commerceLayer/latest/actions/create-tax-category
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Commerce Layer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/commerceLayer/latest/actions/create-tax-category" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "code": "31000",
  "skuId": "WprzSDwgkm",
  "taxCalculatorId": "gvGBQTPANo"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/commerceLayer/latest/actions/create-tax-category', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "code": "31000",
    "skuId": "WprzSDwgkm",
    "taxCalculatorId": "gvGBQTPANo"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `code` | string | yes | The tax category code. Example: `31000`. |
| `skuId` | string | yes | The ID of the SKU to link to this tax category. Example: `WprzSDwgkm`. |
| `taxCalculatorId` | string | yes | The ID of the tax calculator to link to this tax category. Example: `gvGBQTPANo`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `reference` | string | no | An external reference for the tax category. Example: `MC-TAX-CATEGORY`. |
| `referenceOrigin` | string | no | The origin of the external reference. Example: `mindcloud-wizard`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {
        "code": "string",
        "created_at": "2026-05-07T12:00:00.000Z",
        "reference": "string",
        "reference_origin": "string",
        "sku_code": "string",
        "updated_at": "2026-05-07T12:00:00.000Z"
      },
      "id": "string",
      "links": {
        "self": "https://example.com"
      },
      "meta": {
        "mode": "string",
        "organization_id": "string",
        "trace_id": "string"
      },
      "relationships": {
        "attachments": {
          "links": {
            "related": "https://example.com",
            "self": "https://example.com"
          }
        },
        "event_stores": {
          "links": {
            "related": "https://example.com",
            "self": "https://example.com"
          }
        },
        "sku": {
          "links": {
            "related": "https://example.com",
            "self": "https://example.com"
          }
        },
        "tax_calculator": {
          "links": {
            "related": "https://example.com",
            "self": "https://example.com"
          }
        },
        "versions": {
          "links": {
            "related": "https://example.com",
            "self": "https://example.com"
          }
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
| `attributes.code` | string |  |
| `attributes.created_at` | date |  |
| `attributes.reference` | string |  |
| `attributes.reference_origin` | string |  |
| `attributes.sku_code` | string |  |
| `attributes.updated_at` | date |  |
| `id` | string |  |
| `links.self` | string |  |
| `meta.mode` | string |  |
| `meta.organization_id` | string |  |
| `meta.trace_id` | string |  |
| `relationships.attachments.links.related` | string |  |
| `relationships.attachments.links.self` | string |  |
| `relationships.event_stores.links.related` | string |  |
| `relationships.event_stores.links.self` | string |  |
| `relationships.sku.links.related` | string |  |
| `relationships.sku.links.self` | string |  |
| `relationships.tax_calculator.links.related` | string |  |
| `relationships.tax_calculator.links.self` | string |  |
| `relationships.versions.links.related` | string |  |
| `relationships.versions.links.self` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Commerce Layer API, this operation is `POST /api/tax_categories` (base URL `{{credentials.coreApiEndpoint}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-tax-category.md) for the provider-specific parameters and requirements.

