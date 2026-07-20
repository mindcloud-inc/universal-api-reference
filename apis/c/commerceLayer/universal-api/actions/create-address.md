# Commerce Layer: Create Address



```
POST https://connect.mindcloud.co/v1/universal/commerceLayer/latest/actions/create-address
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Commerce Layer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/commerceLayer/latest/actions/create-address" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "firstName": "John",
  "lastName": "Smith",
  "line1": "2883 Geraldine Lane",
  "city": "New York",
  "zipCode": "10013",
  "countryCode": "US",
  "phone": "+12126463381228"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/commerceLayer/latest/actions/create-address', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "firstName": "John",
    "lastName": "Smith",
    "line1": "2883 Geraldine Lane",
    "city": "New York",
    "zipCode": "10013",
    "countryCode": "US",
    "phone": "+12126463381228"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `business` | boolean | no | Whether the address belongs to a business. Default: `false`. Example: `false`. |
| `firstName` | string | yes | The first name for the address contact. Example: `John`. |
| `lastName` | string | yes | The last name for the address contact. Example: `Smith`. |
| `line1` | string | yes | The first address line. Example: `2883 Geraldine Lane`. |
| `city` | string | yes | The city for the address. Example: `New York`. |
| `zipCode` | string | yes | The postal code for the address. Example: `10013`. |
| `countryCode` | string | yes | The ISO country code for the address. Example: `US`. |
| `phone` | string | yes | The phone number for the address contact. Example: `+12126463381228`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `company` | string | no | The company name for a business address. Example: `The Red Brand Inc.`. |
| `line2` | string | no | The second address line. Example: `Apt. 23`. |
| `stateCode` | string | no | The state or province code for the address. Example: `NY`. |
| `email` | string | no | The email address for the address contact. Example: `john@example.com`. |
| `notes` | string | no | Additional notes for the address. Example: `Please ring the bell twice`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {
        "billing_info": "string",
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
| `attributes.billing_info` | string |  |
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

Through the native Commerce Layer API, this operation is `POST /api/addresses` (base URL `{{credentials.coreApiEndpoint}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-address.md) for the provider-specific parameters and requirements.

