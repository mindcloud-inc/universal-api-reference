# Veterans Affairs Facilities: Get Facility

Retrieves a VA facility by ID.

```
GET https://connect.mindcloud.co/v1/universal/veteransAffairsFacilities/latest/actions/get-facility
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Veterans Affairs Facilities `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/veteransAffairsFacilities/latest/actions/get-facility?connectionId=$CONNECTION_ID&facilityId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "facilityId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/veteransAffairsFacilities/latest/actions/get-facility?${params}`, {
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
| `facilityId` | string | yes | Facility ID in the form prefix_station, such as vha_688. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {
        "address": {
          "physical": {
            "address1": "string",
            "city": "string",
            "state": "string",
            "zip": "string"
          }
        },
        "classification": "string",
        "facilityType": "string",
        "hours": {
          "friday": "string",
          "monday": "string",
          "saturday": "string",
          "sunday": "string",
          "thursday": "string",
          "tuesday": "string",
          "wednesday": "string"
        },
        "lat": 1,
        "long": 1,
        "mobile": true,
        "name": "Ava Chen",
        "phone": {
          "fax": "string",
          "main": "string"
        },
        "services": [
          {}
        ],
        "timeZone": "string",
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
| `attributes.address.physical.address1` | string | Street address. |
| `attributes.address.physical.city` | string | City. |
| `attributes.address.physical.state` | string | State. |
| `attributes.address.physical.zip` | string | ZIP code. |
| `attributes.classification` | string | Facility classification. |
| `attributes.facilityType` | string | VA facility type. |
| `attributes.hours.friday` | string | Friday hours. |
| `attributes.hours.monday` | string | Monday hours. |
| `attributes.hours.saturday` | string | Saturday hours. |
| `attributes.hours.sunday` | string | Sunday hours. |
| `attributes.hours.thursday` | string | Thursday hours. |
| `attributes.hours.tuesday` | string | Tuesday hours. |
| `attributes.hours.wednesday` | string | Wednesday hours. |
| `attributes.lat` | number | Facility latitude. |
| `attributes.long` | number | Facility longitude. |
| `attributes.mobile` | boolean | Whether the facility is mobile. |
| `attributes.name` | string | Facility name. |
| `attributes.phone.fax` | string | Fax number. |
| `attributes.phone.main` | string | Main phone number. |
| `attributes.services` | array<object> | Available service records. |
| `attributes.timeZone` | string | Facility time zone. |
| `attributes.website` | string | VA.gov facility page URL. |
| `id` | string | VA facility ID. |
| `type` | string | JSON API resource type. |

## Native endpoint

Through the native Veterans Affairs Facilities API, this operation is `GET /facilities/:facilityId` (base URL `https://sandbox-api.va.gov/services/va_facilities/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-facility.md) for the provider-specific parameters and requirements.

