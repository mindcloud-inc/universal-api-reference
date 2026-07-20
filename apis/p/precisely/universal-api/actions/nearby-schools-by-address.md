# Precisely: Nearby Schools By Address

Retrieves nearby schools from Precisely by address.

```
GET https://connect.mindcloud.co/v1/universal/precisely/latest/actions/nearby-schools-by-address
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Precisely `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/precisely/latest/actions/nearby-schools-by-address?connectionId=$CONNECTION_ID&address=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "address": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/precisely/latest/actions/nearby-schools-by-address?${params}`, {
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
| `address` | string | yes | Single-line street address to search near. |
| `schoolType` | string | no | Provider school type code filter. |
| `edLevel` | string | no | Provider education level code filter. |
| `schoolSubType` | string | no | Provider school subtype code filter. |
| `gender` | string | no | Provider gender code filter. |
| `assignedSchoolsOnly` | boolean | no | Return only schools assigned to the address. |
| `districtSchoolsOnly` | boolean | no | Return only schools in the serving district. |
| `searchRadius` | number | no | Radius around the address to search. |
| `searchRadiusUnit` | string | no | Unit for the search radius. |
| `travelTime` | number | no | Travel time threshold around the address. |
| `travelTimeUnit` | string | no | Unit for the travel time. |
| `travelMode` | string | no | Travel mode used for school proximity calculations. |
| `travelDistance` | number | no | Travel distance threshold around the address. |
| `travelDistanceUnit` | string | no | Unit for the travel distance. |
| `maxCandidates` | number | no | Maximum number of schools to return. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": {
        "areaName1": "Ava Chen",
        "areaName3": "Ava Chen",
        "mainAddressLine": "string",
        "postCode": "string"
      },
      "assigned": "string",
      "distance": {
        "unit": "string",
        "value": "string"
      },
      "educationLevel": "string",
      "educationLevelDesc": "string",
      "geometry": {
        "coordinates": [
          1
        ],
        "type": "string"
      },
      "highestGrade": "string",
      "id": "string",
      "lowestGrade": "string",
      "name": "Ava Chen",
      "ncesDistrictId": "string",
      "ncesSchoolId": "string",
      "phone": "string",
      "schoolSubType": "string",
      "schoolSubTypeDesc": "string",
      "schoolType": "string",
      "schoolTypeDesc": "string",
      "students": "string",
      "studentTeacherRatio": "string",
      "teachers": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address.areaName1` | string | State or province for the school. |
| `address.areaName3` | string | City for the school. |
| `address.mainAddressLine` | string | Primary address line for the school. |
| `address.postCode` | string | Postal code for the school. |
| `assigned` | string | Whether the school is assigned to the queried address. |
| `distance.unit` | string | Unit used for the distance from the queried address. |
| `distance.value` | string | Distance from the queried address to the school. |
| `educationLevel` | string | Provider education-level code. |
| `educationLevelDesc` | string | Education-level label. |
| `geometry.coordinates` | array<number> | Longitude and latitude coordinates for the school location. |
| `geometry.type` | string | GeoJSON geometry type for the school location. |
| `highestGrade` | string | Highest grade served by the school. |
| `id` | string | Provider school identifier. |
| `lowestGrade` | string | Lowest grade served by the school. |
| `name` | string | School name. |
| `ncesDistrictId` | string | NCES district identifier. |
| `ncesSchoolId` | string | NCES school identifier. |
| `phone` | string | School phone number. |
| `schoolSubType` | string | Provider school subtype code. |
| `schoolSubTypeDesc` | string | School subtype label. |
| `schoolType` | string | Provider school type code. |
| `schoolTypeDesc` | string | School type label. |
| `students` | string | Reported student enrollment. |
| `studentTeacherRatio` | string | Reported student-to-teacher ratio. |
| `teachers` | string | Reported teacher count. |

## Native endpoint

Through the native Precisely API, this operation is `GET /schools/v1/school/byaddress` (base URL `https://api.precisely.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/nearby-schools-by-address.md) for the provider-specific parameters and requirements.

