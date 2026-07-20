# Commerce Layer: List Tax Calculators



```
GET https://connect.mindcloud.co/v1/universal/commerceLayer/latest/actions/list-tax-calculators
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Commerce Layer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/commerceLayer/latest/actions/list-tax-calculators?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/commerceLayer/latest/actions/list-tax-calculators?${params}`, {
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
        "commit_invoice": true,
        "company_code": "string",
        "created_at": "2026-05-07T12:00:00.000Z",
        "ddp": true,
        "name": "Ava Chen",
        "reference": "string",
        "reference_origin": "string",
        "type": "string",
        "updated_at": "2026-05-07T12:00:00.000Z",
        "username": "Ava Chen"
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
        "events": {
          "links": {
            "related": "https://example.com",
            "self": "https://example.com"
          }
        },
        "markets": {
          "links": {
            "related": "https://example.com",
            "self": "https://example.com"
          }
        },
        "tax_categories": {
          "links": {
            "related": "https://example.com",
            "self": "https://example.com"
          }
        },
        "tax_rules": {
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
| `attributes.commit_invoice` | boolean |  |
| `attributes.company_code` | string |  |
| `attributes.created_at` | date |  |
| `attributes.ddp` | boolean |  |
| `attributes.name` | string |  |
| `attributes.reference` | string |  |
| `attributes.reference_origin` | string |  |
| `attributes.type` | string |  |
| `attributes.updated_at` | date |  |
| `attributes.username` | string |  |
| `id` | string |  |
| `links.self` | string |  |
| `meta.mode` | string |  |
| `meta.organization_id` | string |  |
| `meta.trace_id` | string |  |
| `relationships.attachments.links.related` | string |  |
| `relationships.attachments.links.self` | string |  |
| `relationships.event_stores.links.related` | string |  |
| `relationships.event_stores.links.self` | string |  |
| `relationships.events.links.related` | string |  |
| `relationships.events.links.self` | string |  |
| `relationships.markets.links.related` | string |  |
| `relationships.markets.links.self` | string |  |
| `relationships.tax_categories.links.related` | string |  |
| `relationships.tax_categories.links.self` | string |  |
| `relationships.tax_rules.links.related` | string |  |
| `relationships.tax_rules.links.self` | string |  |
| `relationships.versions.links.related` | string |  |
| `relationships.versions.links.self` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Commerce Layer API, this operation is `GET /api/tax_calculators` (base URL `{{credentials.coreApiEndpoint}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-tax-calculators.md) for the provider-specific parameters and requirements.

