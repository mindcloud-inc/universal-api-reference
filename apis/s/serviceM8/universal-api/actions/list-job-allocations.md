# ServiceM8: List Job Allocations



```
GET https://connect.mindcloud.co/v1/universal/serviceM8/latest/actions/list-job-allocations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ServiceM8 `connectionId` ([setup](../authentication.md)).

This action also supports [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/serviceM8/latest/actions/list-job-allocations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/serviceM8/latest/actions/list-job-allocations?${params}`, {
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
      "acceptanceStatus": "string",
      "acceptanceTimestamp": "2026-05-07T12:00:00.000Z",
      "active": 1,
      "allocatedByStaffUuid": "string",
      "allocatedTimestamp": "2026-05-07T12:00:00.000Z",
      "allocationDate": "2026-05-07T12:00:00.000Z",
      "allocationWindowUuid": "string",
      "completionTimestamp": "2026-05-07T12:00:00.000Z",
      "editDate": "2026-05-07T12:00:00.000Z",
      "estimatedDuration": "string",
      "expiryTimestamp": "2026-05-07T12:00:00.000Z",
      "jobUuid": "string",
      "queueUuid": "string",
      "readTimestamp": "2026-05-07T12:00:00.000Z",
      "requiresAcceptance": "string",
      "revisedDuration": "string",
      "sortPriority": "string",
      "staffUuid": "string",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `acceptanceStatus` | string | Deprecated acceptance status field. |
| `acceptanceTimestamp` | date | Deprecated acceptance timestamp field. |
| `active` | number | Record active or deleted flag. |
| `allocatedByStaffUuid` | string | UUID of the staff member who allocated the job. |
| `allocatedTimestamp` | date | Timestamp when the allocation was created. |
| `allocationDate` | date | Minimum completion date for the allocation. |
| `allocationWindowUuid` | string | UUID of the allocation window. |
| `completionTimestamp` | date | Timestamp when the allocation was marked completed. |
| `editDate` | date | Timestamp when the allocation was last modified. |
| `estimatedDuration` | string | Deprecated estimated duration field. |
| `expiryTimestamp` | date | Timestamp when the allocation expires. |
| `jobUuid` | string | UUID of the related job. |
| `queueUuid` | string | Deprecated queue UUID for the allocation. |
| `readTimestamp` | date | Timestamp when the allocation was read. |
| `requiresAcceptance` | string | Deprecated acceptance requirement field. |
| `revisedDuration` | string | Deprecated revised duration field. |
| `sortPriority` | string | Sort priority for displaying the allocation. |
| `staffUuid` | string | UUID of the assigned staff member. |
| `uuid` | string | Unique identifier for the allocation. |

## Native endpoint

Through the native ServiceM8 API, this operation is `GET /api_1.0/joballocation.json` (base URL `https://api.servicem8.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-job-allocations.md) for the provider-specific parameters and requirements.

