# Commerce Layer: Update Price List



```
PUT https://connect.mindcloud.co/v1/universal/commerceLayer/latest/actions/update-price-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Commerce Layer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/commerceLayer/latest/actions/update-price-list" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "KLgaxCEPkb",
  "resourceId": "KLgaxCEPkb"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/commerceLayer/latest/actions/update-price-list', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "KLgaxCEPkb",
    "resourceId": "KLgaxCEPkb"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The price list ID to update. Example: `KLgaxCEPkb`. |
| `resourceId` | string | yes | Use the same price list ID in the request body resource object. Example: `KLgaxCEPkb`. |
| `name` | string | no | The updated price list name. Example: `MindCloud Updated Price List`. |
| `currencyCode` | string | no | The updated ISO currency code. Example: `USD`. |
| `taxIncluded` | boolean | no | Whether prices are tax included. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `code` | string | no | The updated price list code. Example: `mc-updated-price-list`. |
| `reference` | string | no | The updated external reference. Example: `MC-UPDATED-PRICE-LIST`. |
| `referenceOrigin` | string | no | The updated external reference origin. Example: `mindcloud-wizard`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {
        "code": "string",
        "created_at": "2026-05-07T12:00:00.000Z",
        "currency_code": "string",
        "name": "Ava Chen",
        "reference": "string",
        "reference_origin": "string",
        "tax_included": true,
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
        "price_list_schedulers": {
          "links": {
            "related": "https://example.com",
            "self": "https://example.com"
          }
        },
        "prices": {
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
| `attributes.currency_code` | string |  |
| `attributes.name` | string |  |
| `attributes.reference` | string |  |
| `attributes.reference_origin` | string |  |
| `attributes.tax_included` | boolean |  |
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
| `relationships.price_list_schedulers.links.related` | string |  |
| `relationships.price_list_schedulers.links.self` | string |  |
| `relationships.prices.links.related` | string |  |
| `relationships.prices.links.self` | string |  |
| `relationships.versions.links.related` | string |  |
| `relationships.versions.links.self` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Commerce Layer API, this operation is `PATCH /api/price_lists/:id` (base URL `{{credentials.coreApiEndpoint}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-price-list.md) for the provider-specific parameters and requirements.

