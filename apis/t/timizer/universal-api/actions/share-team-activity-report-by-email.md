# Timizer: Share Team Activity Report by Email

Shares a team activity report by email in Timizer.

```
POST https://connect.mindcloud.co/v1/universal/timizer/latest/actions/share-team-activity-report-by-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Timizer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/timizer/latest/actions/share-team-activity-report-by-email" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "activityReportId": 1,
  "teamId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/timizer/latest/actions/share-team-activity-report-by-email', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "activityReportId": 1,
    "teamId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `activityReportId` | number | yes | ID of the activity report. |
| `contactId` | number | no | Optional contact ID. Defaults to the activity report client contact. |
| `teamId` | number | yes | ID of the team. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean |  |

## Native endpoint

Through the native Timizer API, this operation is `POST /app/admin-teams/:teamId/activity-reports/:activityReportId/share-by-email` (base URL `https://api.timizer.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/share-team-activity-report-by-email.md) for the provider-specific parameters and requirements.

