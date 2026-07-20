# Storerocket: Get Location



```
GET https://connect.mindcloud.co/v1/universal/storerocket/latest/actions/get-location
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Storerocket `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/storerocket/latest/actions/get-location?connectionId=$CONNECTION_ID&projectId=string&locationId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "string",
  "locationId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/storerocket/latest/actions/get-location?${params}`, {
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
| `projectId` | string | yes | The StoreRocket project ID that owns the location. |
| `locationId` | string | yes | The StoreRocket location ID. |

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

Through the native Storerocket API, this operation is `GET /projects/:projectId/locations/:locationId` (base URL `https://storerocket.io/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-location.md) for the provider-specific parameters and requirements.

