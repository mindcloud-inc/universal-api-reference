# FEMA: List Training Class Schedule

Retrieves the FEMA training class schedule.

```
GET https://connect.mindcloud.co/v1/universal/fEMA/latest/actions/list-training-class-schedule
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FEMA `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fEMA/latest/actions/list-training-class-schedule?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fEMA/latest/actions/list-training-class-schedule?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "classEndDatetime": "2026-05-07T12:00:00.000Z",
      "classID": "string",
      "classLocationCity": "string",
      "classLocationName": "Ava Chen",
      "classLocationState": "string",
      "classPOCEmail": "ava@example.com",
      "classPOCName": "Ava Chen",
      "classPOCPhone": "string",
      "classRegistrationCloseDate": "2026-05-07T12:00:00.000Z",
      "classRegistrationOpenDate": "2026-05-07T12:00:00.000Z",
      "classRegistrationRequired": true,
      "classRegistrationURL": "https://example.com",
      "classStartDatetime": "2026-05-07T12:00:00.000Z",
      "classTimeZone": "string",
      "classTrainingProvider": "string",
      "courseCatalogNumber": "string",
      "courseID": "string",
      "dataSource": "string",
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `classEndDatetime` | date |  |
| `classID` | string |  |
| `classLocationCity` | string |  |
| `classLocationName` | string |  |
| `classLocationState` | string |  |
| `classPOCEmail` | string |  |
| `classPOCName` | string |  |
| `classPOCPhone` | string |  |
| `classRegistrationCloseDate` | date |  |
| `classRegistrationOpenDate` | date |  |
| `classRegistrationRequired` | boolean |  |
| `classRegistrationURL` | string |  |
| `classStartDatetime` | date |  |
| `classTimeZone` | string |  |
| `classTrainingProvider` | string |  |
| `courseCatalogNumber` | string |  |
| `courseID` | string |  |
| `dataSource` | string |  |
| `id` | string |  |

## Native endpoint

Through the native FEMA API, this operation is `GET /v1/TrainingClassSchedule` (base URL `https://www.fema.gov/api/open`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-training-class-schedule.md) for the provider-specific parameters and requirements.

