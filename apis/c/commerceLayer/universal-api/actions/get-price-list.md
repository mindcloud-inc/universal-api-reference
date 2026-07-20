# Commerce Layer: Get Price List



```
GET https://connect.mindcloud.co/v1/universal/commerceLayer/latest/actions/get-price-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Commerce Layer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/commerceLayer/latest/actions/get-price-list?connectionId=$CONNECTION_ID&id=dBvwGCrgkz" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "dBvwGCrgkz"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/commerceLayer/latest/actions/get-price-list?${params}`, {
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
| `id` | string | yes | The ID of the price list to retrieve. Example: `dBvwGCrgkz`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {
        "created_at": "2026-05-07T12:00:00.000Z",
        "currency_code": "string",
        "name": "Ava Chen",
        "rule_outcomes": [
          "string"
        ],
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
| `attributes.created_at` | date |  |
| `attributes.currency_code` | string |  |
| `attributes.name` | string |  |
| `attributes.rule_outcomes[]` | string |  |
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

Through the native Commerce Layer API, this operation is `GET /api/price_lists/:id` (base URL `{{credentials.coreApiEndpoint}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-price-list.md) for the provider-specific parameters and requirements.

