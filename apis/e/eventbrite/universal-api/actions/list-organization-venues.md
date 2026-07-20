# Eventbrite: List Organization Venues

Retrieves organization venues from Eventbrite.

```
GET https://connect.mindcloud.co/v1/universal/eventbrite/latest/actions/list-organization-venues
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Eventbrite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eventbrite/latest/actions/list-organization-venues?connectionId=$CONNECTION_ID&organizationId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organizationId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eventbrite/latest/actions/list-organization-venues?${params}`, {
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
| `organizationId` | string | yes | Organization identifier. |

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

Through the native Eventbrite API, this operation is `GET /organizations/:organizationId/venues/` (base URL `https://www.eventbriteapi.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-organization-venues.md) for the provider-specific parameters and requirements.

