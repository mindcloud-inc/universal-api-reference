# Toggl Track: Search Detailed Report

Finds detailed report time entries in Toggl Track.

```
GET https://connect.mindcloud.co/v1/universal/togglTrack/latest/actions/search-detailed-report
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Toggl Track `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/togglTrack/latest/actions/search-detailed-report?connectionId=$CONNECTION_ID&workspaceId=1&startDate=string&endDate=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workspaceId": "1",
  "startDate": "string",
  "endDate": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/togglTrack/latest/actions/search-detailed-report?${params}`, {
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
| `workspaceId` | list<number> | yes |  |
| `startDate` | string | yes |  |
| `endDate` | string | yes |  |
| `pageSize` | number | no |  |
| `orderBy` | string | no |  |
| `orderDir` | string | no |  |
| `description` | string | no |  |
| `billable` | boolean | no |  |
| `grouped` | boolean | no |  |
| `hideAmounts` | boolean | no |  |
| `enrichResponse` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "billable": true,
      "billableAmountInCents": {},
      "currency": "string",
      "description": "string",
      "hourlyRateInCents": {},
      "projectId": {},
      "rowNumber": 1,
      "taskId": {},
      "timeEntries": [
        {
          "at": "string",
          "atTz": "string",
          "id": 1,
          "seconds": 1,
          "start": "string",
          "stop": "string"
        }
      ],
      "togglAccountsId": "string",
      "userId": 1,
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `billable` | boolean |  |
| `billableAmountInCents` | object |  |
| `currency` | string |  |
| `description` | string |  |
| `hourlyRateInCents` | object |  |
| `projectId` | object |  |
| `rowNumber` | number |  |
| `taskId` | object |  |
| `timeEntries[].at` | string |  |
| `timeEntries[].atTz` | string |  |
| `timeEntries[].id` | number |  |
| `timeEntries[].seconds` | number |  |
| `timeEntries[].start` | string |  |
| `timeEntries[].stop` | string |  |
| `togglAccountsId` | string |  |
| `userId` | number |  |
| `username` | string |  |

## Native endpoint

Through the native Toggl Track API, this operation is `POST /reports/api/v3/workspace/:workspace_id/search/time_entries` (base URL `https://api.track.toggl.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-detailed-report.md) for the provider-specific parameters and requirements.

