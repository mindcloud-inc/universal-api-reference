# ServiceTitan: Get Jobs



```
GET https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/job-planning-get-jobs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ServiceTitan `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/job-planning-get-jobs?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/job-planning-get-jobs?${params}`, {
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
| `bookingId` | number | no | Filters by booking ID that resulted in this job |
| `projectId` | number | no | Filters by project ID |
| `locationId` | number | no | Filters by job's location ID |
| `customerId` | number | no | Filters by job's customer ID |
| `ids` | string | no |  |
| `number` | string | no |  |
| `firstAppointmentStartsOnOrAfter` | string | no |  |
| `firstAppointmentStartsBefore` | string | no |  |
| `appointmentStartsOnOrAfter` | string | no |  |
| `appointmentStartsBefore` | string | no |  |
| `createdBefore` | string | no |  |
| `createdOnOrAfter` | string | no |  |
| `modifiedBefore` | string | no |  |
| `modifiedOnOrAfter` | string | no |  |
| `completedOnOrAfter` | string | no |  |
| `completedBefore` | string | no |  |
| `sort` | string | no |  |
| `externalDataApplicationGuid` | string | no |  |
| `externalDataKey` | string | no |  |
| `externalDataValues` | string | no |  |
| `jobStatus` | list<string> | no | Filters by job status Values: [Scheduled, Dispatched, InProgress, Hold, Completed, Canceled] |
| `appointmentStatus` | string | no |  |
| `priority` | string | no |  |
| `technicianId` | number | no |  |
| `soldById` | number | no |  |
| `jobTypeId` | number | no |  |
| `campaignId` | number | no |  |
| `businessUnitId` | number | no |  |
| `invoiceId` | number | no |  |
| `tagTypeIds` | string | no |  |
| `hasUnusedAppointments` | boolean | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ServiceTitan API returns.

## Native endpoint

Through the native ServiceTitan API, this operation is `GET https://api.servicetitan.io/jpm/v2/tenant/{{credentials.tenant}}/jobs` (base URL `https://{{credentials.baseUrl}}/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/job-planning-get-jobs.md) for the provider-specific parameters and requirements.

