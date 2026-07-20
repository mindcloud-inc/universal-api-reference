# Storerocket: Update Location



```
PUT https://connect.mindcloud.co/v1/universal/storerocket/latest/actions/update-location
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Storerocket `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/storerocket/latest/actions/update-location" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": "string",
  "locationId": "string",
  "name": "Ava Chen",
  "addressLine1": "string",
  "city": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/storerocket/latest/actions/update-location', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": "string",
    "locationId": "string",
    "name": "Ava Chen",
    "addressLine1": "string",
    "city": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `projectId` | string | yes | The StoreRocket project ID that owns the location. |
| `locationId` | string | yes | The StoreRocket location ID. |
| `name` | string | yes | Location display name. |
| `addressLine1` | string | yes | Primary street address for the location. |
| `addressLine2` | string | no | Secondary street address details. |
| `city` | string | yes | City for the location. |
| `postcode` | string | no | Postal code. |
| `country` | string | no | Country code or name. |
| `state` | string | no | State or region. |
| `phone` | string | no | Contact phone number. |
| `email` | string | no | Contact email address. |
| `url` | string | no | Public website URL for the location. |
| `facebook` | string | no | Facebook profile URL. |
| `instagram` | string | no | Instagram profile URL. |
| `twitter` | string | no | Twitter/X profile URL. |
| `yelp` | string | no | Yelp page URL. |
| `visible` | boolean | no | Whether the location is visible in the locator. |
| `lat` | number | no | Latitude override for the location. |
| `lng` | number | no | Longitude override for the location. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": "string",
      "addressLine1": "string",
      "addressLine2": "string",
      "callsToAction": [
        {}
      ],
      "city": "string",
      "country": "string",
      "coverImageUrl": "https://example.com",
      "displayAddress": "string",
      "email": "ava@example.com",
      "facebook": "string",
      "fields": [
        {}
      ],
      "filters": [
        {}
      ],
      "hours": {},
      "id": "string",
      "instagram": "string",
      "lat": 1,
      "lng": 1,
      "locationType": "string",
      "markerUrl": "https://example.com",
      "name": "Ava Chen",
      "phone": "string",
      "postcode": "string",
      "slug": "string",
      "state": "string",
      "twitter": "string",
      "url": "https://example.com",
      "visible": true,
      "yelp": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | string |  |
| `addressLine1` | string |  |
| `addressLine2` | string |  |
| `callsToAction` | array<object> |  |
| `city` | string |  |
| `country` | string |  |
| `coverImageUrl` | string |  |
| `displayAddress` | string |  |
| `email` | string |  |
| `facebook` | string |  |
| `fields` | array<object> |  |
| `filters` | array<object> |  |
| `hours` | object |  |
| `id` | string |  |
| `instagram` | string |  |
| `lat` | number |  |
| `lng` | number |  |
| `locationType` | string |  |
| `markerUrl` | string |  |
| `name` | string |  |
| `phone` | string |  |
| `postcode` | string |  |
| `slug` | string |  |
| `state` | string |  |
| `twitter` | string |  |
| `url` | string |  |
| `visible` | boolean |  |
| `yelp` | string |  |

## Native endpoint

Through the native Storerocket API, this operation is `PUT /projects/:projectId/locations/:locationId` (base URL `https://storerocket.io/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-location.md) for the provider-specific parameters and requirements.

