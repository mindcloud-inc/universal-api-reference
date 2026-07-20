# Commerce Layer: Update Address



```
PUT https://connect.mindcloud.co/v1/universal/commerceLayer/latest/actions/update-address
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Commerce Layer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/commerceLayer/latest/actions/update-address" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "dJeJuqpoaJ",
  "resourceId": "dJeJuqpoaJ"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/commerceLayer/latest/actions/update-address', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "dJeJuqpoaJ",
    "resourceId": "dJeJuqpoaJ"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The address ID to update. Example: `dJeJuqpoaJ`. |
| `resourceId` | string | yes | The address resource ID in the JSON:API body. Use the same value as Address ID. Example: `dJeJuqpoaJ`. |
| `firstName` | string | no | The updated first name. Example: `Avery`. |
| `lastName` | string | no | The updated last name. Example: `Marketmaker`. |
| `phone` | string | no | The updated phone number. Example: `+12125550203`. |
| `email` | string | no | The updated email address. Example: `avery.updated@example.com`. |
| `notes` | string | no | The updated notes. Example: `Updated by MindCloud wizard`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {
        "business": true,
        "city": "string",
        "company": "string",
        "country_code": "string",
        "created_at": "2026-05-07T12:00:00.000Z",
        "email": "ava@example.com",
        "first_name": "Ava",
        "full_address": "string",
        "full_name": "Ava Chen",
        "is_geocoded": true,
        "is_localized": true,
        "last_name": "Chen",
        "lat": 1,
        "line_1": "string",
        "line_2": "string",
        "lng": 1,
        "map_url": "https://example.com",
        "name": "Ava Chen",
        "notes": "string",
        "phone": "string",
        "provider_name": "Ava Chen",
        "reference": "string",
        "reference_origin": "string",
        "state_code": "string",
        "static_map_url": "https://example.com",
        "updated_at": "2026-05-07T12:00:00.000Z",
        "zip_code": "string"
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
        "events": {
          "links": {
            "related": "https://example.com",
            "self": "https://example.com"
          }
        },
        "geocoder": {
          "links": {
            "related": "https://example.com",
            "self": "https://example.com"
          }
        },
        "tags": {
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
| `attributes.business` | boolean |  |
| `attributes.city` | string |  |
| `attributes.company` | string |  |
| `attributes.country_code` | string |  |
| `attributes.created_at` | date |  |
| `attributes.email` | string |  |
| `attributes.first_name` | string |  |
| `attributes.full_address` | string |  |
| `attributes.full_name` | string |  |
| `attributes.is_geocoded` | boolean |  |
| `attributes.is_localized` | boolean |  |
| `attributes.last_name` | string |  |
| `attributes.lat` | number |  |
| `attributes.line_1` | string |  |
| `attributes.line_2` | string |  |
| `attributes.lng` | number |  |
| `attributes.map_url` | string |  |
| `attributes.name` | string |  |
| `attributes.notes` | string |  |
| `attributes.phone` | string |  |
| `attributes.provider_name` | string |  |
| `attributes.reference` | string |  |
| `attributes.reference_origin` | string |  |
| `attributes.state_code` | string |  |
| `attributes.static_map_url` | string |  |
| `attributes.updated_at` | date |  |
| `attributes.zip_code` | string |  |
| `id` | string |  |
| `links.self` | string |  |
| `meta.mode` | string |  |
| `meta.organization_id` | string |  |
| `meta.trace_id` | string |  |
| `relationships.event_stores.links.related` | string |  |
| `relationships.event_stores.links.self` | string |  |
| `relationships.events.links.related` | string |  |
| `relationships.events.links.self` | string |  |
| `relationships.geocoder.links.related` | string |  |
| `relationships.geocoder.links.self` | string |  |
| `relationships.tags.links.related` | string |  |
| `relationships.tags.links.self` | string |  |
| `relationships.versions.links.related` | string |  |
| `relationships.versions.links.self` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Commerce Layer API, this operation is `PATCH /api/addresses/:id` (base URL `{{credentials.coreApiEndpoint}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-address.md) for the provider-specific parameters and requirements.

