# Recreation.gov: Get Rec Area

Retrieves a recreation area from Recreation.gov.

```
GET https://connect.mindcloud.co/v1/universal/recreationgov/latest/actions/get-rec-area
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Recreation.gov `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/recreationgov/latest/actions/get-rec-area?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/recreationgov/latest/actions/get-rec-area?${params}`, {
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
      "Keywords": "string",
      "LastUpdatedDate": "string",
      "OrgRecAreaID": "string",
      "ParentOrgID": "string",
      "RecAreaAccessibilityText": "string",
      "RecAreaDescription": "string",
      "RecAreaDirections": "string",
      "RecAreaEmail": "ava@example.com",
      "RecAreaFeeDescription": "string",
      "RecAreaID": "string",
      "RecAreaLatitude": 1,
      "RecAreaLongitude": 1,
      "RecAreaMapURL": "https://example.com",
      "RecAreaName": "Ava Chen",
      "RecAreaPhone": "string",
      "RecAreaReservationURL": "https://example.com",
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
| `Keywords` | string |  |
| `LastUpdatedDate` | string |  |
| `OrgRecAreaID` | string |  |
| `ParentOrgID` | string |  |
| `RecAreaAccessibilityText` | string |  |
| `RecAreaDescription` | string |  |
| `RecAreaDirections` | string |  |
| `RecAreaEmail` | string |  |
| `RecAreaFeeDescription` | string |  |
| `RecAreaID` | string |  |
| `RecAreaLatitude` | number |  |
| `RecAreaLongitude` | number |  |
| `RecAreaMapURL` | string |  |
| `RecAreaName` | string |  |
| `RecAreaPhone` | string |  |
| `RecAreaReservationURL` | string |  |
| `Reservable` | boolean |  |
| `StayLimit` | string |  |

## Native endpoint

Through the native Recreation.gov API, this operation is `GET /recareas/{id}` (base URL `https://ridb.recreation.gov/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-rec-area.md) for the provider-specific parameters and requirements.

