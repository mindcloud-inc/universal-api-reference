# Commerce Layer: Update Manual Tax Calculator



```
PUT https://connect.mindcloud.co/v1/universal/commerceLayer/latest/actions/update-manual-tax-calculator
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Commerce Layer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/commerceLayer/latest/actions/update-manual-tax-calculator" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "AbCdEfGhIj",
  "resourceId": "AbCdEfGhIj"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/commerceLayer/latest/actions/update-manual-tax-calculator', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "AbCdEfGhIj",
    "resourceId": "AbCdEfGhIj"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The manual tax calculator ID to update. Example: `AbCdEfGhIj`. |
| `resourceId` | string | yes | Use the same manual tax calculator ID in the request body resource object. Example: `AbCdEfGhIj`. |
| `name` | string | no | The updated manual tax calculator name. Example: `MindCloud Updated Manual Tax Calculator`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `reference` | string | no | The updated external reference. Example: `MC-UPDATED-MANUAL-TAX-CALCULATOR`. |
| `referenceOrigin` | string | no | The updated external reference origin. Example: `mindcloud-wizard`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {
        "created_at": "2026-05-07T12:00:00.000Z",
        "name": "Ava Chen",
        "reference": "string",
        "reference_origin": "string",
        "type": "string",
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
| `attributes.created_at` | date |  |
| `attributes.name` | string |  |
| `attributes.reference` | string |  |
| `attributes.reference_origin` | string |  |
| `attributes.type` | string |  |
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
| `relationships.events.links.related` | string |  |
| `relationships.events.links.self` | string |  |
| `relationships.markets.links.related` | string |  |
| `relationships.markets.links.self` | string |  |
| `relationships.tax_rules.links.related` | string |  |
| `relationships.tax_rules.links.self` | string |  |
| `relationships.versions.links.related` | string |  |
| `relationships.versions.links.self` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Commerce Layer API, this operation is `PATCH /api/manual_tax_calculators/:id` (base URL `{{credentials.coreApiEndpoint}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-manual-tax-calculator.md) for the provider-specific parameters and requirements.

