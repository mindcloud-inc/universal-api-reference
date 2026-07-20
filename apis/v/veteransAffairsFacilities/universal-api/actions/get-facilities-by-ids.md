# Veterans Affairs Facilities: Get Facilities by IDs

Retrieves VA facilities by facility IDs.

```
GET https://connect.mindcloud.co/v1/universal/veteransAffairsFacilities/latest/actions/get-facilities-by-ids
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Veterans Affairs Facilities `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/veteransAffairsFacilities/latest/actions/get-facilities-by-ids?connectionId=$CONNECTION_ID&ids=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "ids": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/veteransAffairsFacilities/latest/actions/get-facilities-by-ids?${params}`, {
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
| `ids` | string | yes | Comma-separated facility IDs to retrieve, such as vha_688,vha_570. |

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

Through the native Veterans Affairs Facilities API, this operation is `GET /facilities` (base URL `https://sandbox-api.va.gov/services/va_facilities/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-facilities-by-ids.md) for the provider-specific parameters and requirements.

