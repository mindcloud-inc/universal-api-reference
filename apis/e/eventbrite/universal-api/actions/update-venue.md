# Eventbrite: Update Venue

Updates an existing venue in Eventbrite.

```
PUT https://connect.mindcloud.co/v1/universal/eventbrite/latest/actions/update-venue
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Eventbrite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/eventbrite/latest/actions/update-venue" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "venue.address.address1": "string",
  "venue.address.city": "string",
  "venue.address.country": "string",
  "venue.address.postalCode": "string",
  "venue.address.region": "string",
  "venue.name": "Ava Chen",
  "venueId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eventbrite/latest/actions/update-venue', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "venue.address.address1": "string",
    "venue.address.city": "string",
    "venue.address.country": "string",
    "venue.address.postalCode": "string",
    "venue.address.region": "string",
    "venue.name": "Ava Chen",
    "venueId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `venue.address.address1` | string | yes | Street address line 1. |
| `venue.address.city` | string | yes | City. |
| `venue.address.country` | string | yes | Two-letter country code (e.g. US). |
| `venue.address.postalCode` | string | yes | Postal code. |
| `venue.address.region` | string | yes | State/region code. |
| `venue.name` | string | yes | Venue display name. |
| `venueId` | string | yes | Venue identifier. |

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
      "ageRestriction": "string",
      "capacity": 1,
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
| `address` | object | Updated venue address object. |
| `address.address1` | string | Venue street address line 1. |
| `address.address2` | string | Venue street address line 2. |
| `address.city` | string | Venue city. |
| `address.country` | string | Venue country code. |
| `address.latitude` | string | Venue latitude. |
| `address.localizedAddressDisplay` | string | Localized single-line address. |
| `address.localizedAreaDisplay` | string | Localized area display. |
| `address.localizedMultiLineAddressDisplay` | array<string> | Localized multi-line address. |
| `address.longitude` | string | Venue longitude. |
| `address.postalCode` | string | Venue postal code. |
| `address.region` | string | Venue state or region. |
| `ageRestriction` | string | Venue age restriction. |
| `capacity` | number | Venue capacity. |
| `id` | string | Venue identifier. |
| `latitude` | string | Venue latitude. |
| `longitude` | string | Venue longitude. |
| `name` | string | Venue name. |
| `resourceUri` | string | Venue resource URI. |

## Native endpoint

Through the native Eventbrite API, this operation is `POST /venues/:venueId/` (base URL `https://www.eventbriteapi.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-venue.md) for the provider-specific parameters and requirements.

