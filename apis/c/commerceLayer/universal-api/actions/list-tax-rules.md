# Commerce Layer: List Tax Rules



```
GET https://connect.mindcloud.co/v1/universal/commerceLayer/latest/actions/list-tax-rules
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Commerce Layer `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/commerceLayer/latest/actions/list-tax-rules?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/commerceLayer/latest/actions/list-tax-rules?${params}`, {
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
        "adjustment_taxable": true,
        "country_code_regex": "string",
        "created_at": "2026-05-07T12:00:00.000Z",
        "freight_taxable": true,
        "gift_card_taxable": true,
        "name": "Ava Chen",
        "not_country_code_regex": "string",
        "not_state_code_regex": "string",
        "not_zip_code_regex": "string",
        "payment_method_taxable": true,
        "reference": "string",
        "reference_origin": "string",
        "state_code_regex": "string",
        "tax_rate": "string",
        "updated_at": "2026-05-07T12:00:00.000Z",
        "zip_code_regex": "string"
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
        "event_stores": {
          "links": {
            "related": "https://example.com",
            "self": "https://example.com"
          }
        },
        "manual_tax_calculator": {
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
| `attributes.adjustment_taxable` | boolean |  |
| `attributes.country_code_regex` | string |  |
| `attributes.created_at` | date |  |
| `attributes.freight_taxable` | boolean |  |
| `attributes.gift_card_taxable` | boolean |  |
| `attributes.name` | string |  |
| `attributes.not_country_code_regex` | string |  |
| `attributes.not_state_code_regex` | string |  |
| `attributes.not_zip_code_regex` | string |  |
| `attributes.payment_method_taxable` | boolean |  |
| `attributes.reference` | string |  |
| `attributes.reference_origin` | string |  |
| `attributes.state_code_regex` | string |  |
| `attributes.tax_rate` | string |  |
| `attributes.updated_at` | date |  |
| `attributes.zip_code_regex` | string |  |
| `id` | string |  |
| `links.self` | string |  |
| `meta.mode` | string |  |
| `meta.organization_id` | string |  |
| `meta.trace_id` | string |  |
| `relationships.event_stores.links.related` | string |  |
| `relationships.event_stores.links.self` | string |  |
| `relationships.manual_tax_calculator.links.related` | string |  |
| `relationships.manual_tax_calculator.links.self` | string |  |
| `relationships.versions.links.related` | string |  |
| `relationships.versions.links.self` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Commerce Layer API, this operation is `GET /api/tax_rules` (base URL `{{credentials.coreApiEndpoint}}`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-tax-rules.md) for the provider-specific parameters and requirements.

