# Veterans Affairs Facilities: Search Facilities by Bounding Box

Finds VA facilities in a bounding box.

```
GET https://connect.mindcloud.co/v1/universal/veteransAffairsFacilities/latest/actions/search-facilities-by-bounding-box
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Veterans Affairs Facilities `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/veteransAffairsFacilities/latest/actions/search-facilities-by-bounding-box?connectionId=$CONNECTION_ID&limit=25&offset=0&bbox%5B%5D=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "bbox[]": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/veteransAffairsFacilities/latest/actions/search-facilities-by-bounding-box?${params}`, {
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
| `bbox[]` | array<number> | yes | Four bounding-box numbers as west longitude, south latitude, east longitude, north latitude. Accepts multiple values as an array. |
| `type` | list | no | Optional facility type filter. One of: `benefits`, `cemetery`, `health`, `vet_center`. |
| `mobile` | boolean | no | When true, only return mobile facilities. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `services[]` | array<string> | no | Optional VA service identifiers to filter by. Accepts multiple values as an array. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {
        "address": {
          "physical": {
            "city": "string",
            "state": "string",
            "zip": "string"
          }
        },
        "classification": "string",
        "facilityType": "string",
        "lat": 1,
        "long": 1,
        "mobile": true,
        "name": "Ava Chen",
        "phone": {
          "main": "string"
        },
        "website": "https://example.com"
      },
      "id": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes.address.physical.city` | string | City. |
| `attributes.address.physical.state` | string | State. |
| `attributes.address.physical.zip` | string | ZIP code. |
| `attributes.classification` | string | Facility classification. |
| `attributes.facilityType` | string | VA facility type. |
| `attributes.lat` | number | Latitude. |
| `attributes.long` | number | Longitude. |
| `attributes.mobile` | boolean | Whether the facility is mobile. |
| `attributes.name` | string | Facility name. |
| `attributes.phone.main` | string | Main phone number. |
| `attributes.website` | string | VA.gov facility page URL. |
| `id` | string | VA facility ID. |
| `type` | string | JSON API resource type. |

## Native endpoint

Through the native Veterans Affairs Facilities API, this operation is `GET /facilities` (base URL `https://sandbox-api.va.gov/services/va_facilities/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-facilities-by-bounding-box.md) for the provider-specific parameters and requirements.

