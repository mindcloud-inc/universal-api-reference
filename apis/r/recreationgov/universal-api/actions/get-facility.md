# Recreation.gov: Get Facility

Retrieves a facility from Recreation.gov.

```
GET https://connect.mindcloud.co/v1/universal/recreationgov/latest/actions/get-facility
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Recreation.gov `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/recreationgov/latest/actions/get-facility?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/recreationgov/latest/actions/get-facility?${params}`, {
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
| `id` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Enabled": true,
      "FacilityAccessibilityText": "string",
      "FacilityAdaAccess": "string",
      "FacilityDescription": "string",
      "FacilityDirections": "string",
      "FacilityEmail": "ava@example.com",
      "FacilityID": "string",
      "FacilityLatitude": 1,
      "FacilityLongitude": 1,
      "FacilityMapURL": "https://example.com",
      "FacilityName": "Ava Chen",
      "FacilityPhone": "string",
      "FacilityReservationURL": "https://example.com",
      "FacilityTypeDescription": "string",
      "FacilityUseFeeDescription": "string",
      "Keywords": "string",
      "LastUpdatedDate": "string",
      "OrgFacilityID": "string",
      "ParentOrgID": "string",
      "ParentRecAreaID": "string",
      "Reservable": true,
      "StayLimit": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Enabled` | boolean |  |
| `FacilityAccessibilityText` | string |  |
| `FacilityAdaAccess` | string |  |
| `FacilityDescription` | string |  |
| `FacilityDirections` | string |  |
| `FacilityEmail` | string |  |
| `FacilityID` | string |  |
| `FacilityLatitude` | number |  |
| `FacilityLongitude` | number |  |
| `FacilityMapURL` | string |  |
| `FacilityName` | string |  |
| `FacilityPhone` | string |  |
| `FacilityReservationURL` | string |  |
| `FacilityTypeDescription` | string |  |
| `FacilityUseFeeDescription` | string |  |
| `Keywords` | string |  |
| `LastUpdatedDate` | string |  |
| `OrgFacilityID` | string |  |
| `ParentOrgID` | string |  |
| `ParentRecAreaID` | string |  |
| `Reservable` | boolean |  |
| `StayLimit` | string |  |

## Native endpoint

Through the native Recreation.gov API, this operation is `GET /facilities/{id}` (base URL `https://ridb.recreation.gov/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-facility.md) for the provider-specific parameters and requirements.

