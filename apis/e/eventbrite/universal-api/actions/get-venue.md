# Eventbrite: Get Venue

Retrieves a venue from Eventbrite.

```
GET https://connect.mindcloud.co/v1/universal/eventbrite/latest/actions/get-venue
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Eventbrite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eventbrite/latest/actions/get-venue?connectionId=$CONNECTION_ID&venueId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "venueId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eventbrite/latest/actions/get-venue?${params}`, {
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

Through the native Eventbrite API, this operation is `GET /venues/:venueId/` (base URL `https://www.eventbriteapi.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-venue.md) for the provider-specific parameters and requirements.

