# ServiceM8: List Job Activities



```
GET https://connect.mindcloud.co/v1/universal/serviceM8/latest/actions/list-job-activities
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ServiceM8 `connectionId` ([setup](../authentication.md)).

This action also supports [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/serviceM8/latest/actions/list-job-activities?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/serviceM8/latest/actions/list-job-activities?${params}`, {
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
      "active": 1,
      "activityWasAutomated": 1,
      "activityWasRecorded": 1,
      "activityWasScheduled": 1,
      "allocatedByStaffUuid": "string",
      "allocatedTimestamp": "2026-05-07T12:00:00.000Z",
      "editByStaffUuid": "string",
      "editDate": "2026-05-07T12:00:00.000Z",
      "endDate": "2026-05-07T12:00:00.000Z",
      "hasBeenOpened": 1,
      "hasBeenOpenedTimestamp": "2026-05-07T12:00:00.000Z",
      "jobUuid": "string",
      "materialUuid": "string",
      "staffUuid": "string",
      "startDate": "2026-05-07T12:00:00.000Z",
      "travelDistanceInMeters": 1,
      "travelTimeInSeconds": 1,
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | number | Record active or deleted flag. |
| `activityWasAutomated` | number | Flag indicating whether the activity was automated. |
| `activityWasRecorded` | number | Flag indicating whether the activity was recorded after completion. |
| `activityWasScheduled` | number | Flag indicating whether the activity was scheduled in advance. |
| `allocatedByStaffUuid` | string | UUID of the staff member who allocated the activity. |
| `allocatedTimestamp` | date | Timestamp when the activity was allocated. |
| `editByStaffUuid` | string | Staff UUID of the last editor. |
| `editDate` | date | Timestamp when the record was last modified. |
| `endDate` | date | Scheduled end date and time for the activity. |
| `hasBeenOpened` | number | Flag indicating whether the assigned staff member opened the activity. |
| `hasBeenOpenedTimestamp` | date | Timestamp when the assigned staff member first opened the activity. |
| `jobUuid` | string | UUID of the job this activity belongs to. |
| `materialUuid` | string | UUID of the associated material. |
| `staffUuid` | string | UUID of the assigned staff member. |
| `startDate` | date | Scheduled start date and time for the activity. |
| `travelDistanceInMeters` | number | Estimated travel distance in meters. |
| `travelTimeInSeconds` | number | Estimated travel time in seconds. |
| `uuid` | string | Unique identifier for this job activity. |

## Native endpoint

Through the native ServiceM8 API, this operation is `GET /api_1.0/jobactivity.json` (base URL `https://api.servicem8.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-job-activities.md) for the provider-specific parameters and requirements.

