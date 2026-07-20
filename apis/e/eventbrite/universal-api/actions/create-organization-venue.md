# Eventbrite: Create Organization Venue

Creates a new organization venue in Eventbrite.

```
POST https://connect.mindcloud.co/v1/universal/eventbrite/latest/actions/create-organization-venue
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Eventbrite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/eventbrite/latest/actions/create-organization-venue" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "organizationId": "string",
  "venue.address.address1": "string",
  "venue.address.city": "string",
  "venue.address.country": "string",
  "venue.address.postalCode": "string",
  "venue.address.region": "string",
  "venue.name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eventbrite/latest/actions/create-organization-venue', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "organizationId": "string",
    "venue.address.address1": "string",
    "venue.address.city": "string",
    "venue.address.country": "string",
    "venue.address.postalCode": "string",
    "venue.address.region": "string",
    "venue.name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `organizationId` | string | yes | Organization identifier. |
| `venue.address.address1` | string | yes | Street address line 1. |
| `venue.address.city` | string | yes | City. |
| `venue.address.country` | string | yes | Two-letter country code (e.g. US). |
| `venue.address.postalCode` | string | yes | Postal code. |
| `venue.address.region` | string | yes | State/region code. |
| `venue.name` | string | yes | Venue display name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": {
        "address1": "string",
        "address2": "string",
        "city": "string",
        "country": "string",
        "latitude": "string",
        "localizedAddressDisplay": "string",
        "localizedAreaDisplay": "string",
        "localizedMultiLineAddressDisplay": [
          "string"
        ],
        "longitude": "string",
        "postalCode": "string",
        "region": "string"
      },
      "ageRestriction": {},
      "capacity": {},
      "id": "string",
      "latitude": "string",
      "longitude": "string",
      "name": "Ava Chen",
      "resourceUri": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address.address1` | string |  |
| `address.address2` | string |  |
| `address.city` | string |  |
| `address.country` | string |  |
| `address.latitude` | string |  |
| `address.localizedAddressDisplay` | string |  |
| `address.localizedAreaDisplay` | string |  |
| `address.localizedMultiLineAddressDisplay[]` | string |  |
| `address.longitude` | string |  |
| `address.postalCode` | string |  |
| `address.region` | string |  |
| `ageRestriction` | object |  |
| `capacity` | object |  |
| `id` | string |  |
| `latitude` | string |  |
| `longitude` | string |  |
| `name` | string |  |
| `resourceUri` | string |  |

## Native endpoint

Through the native Eventbrite API, this operation is `POST /organizations/:organizationId/venues/` (base URL `https://www.eventbriteapi.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-organization-venue.md) for the provider-specific parameters and requirements.

