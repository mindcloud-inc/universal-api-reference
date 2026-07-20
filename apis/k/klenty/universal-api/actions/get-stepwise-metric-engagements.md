# Klenty: Get Stepwise Metric Engagements

Retrieves stepwise metric engagements from Klenty.

```
GET https://connect.mindcloud.co/v1/universal/klenty/latest/actions/get-stepwise-metric-engagements
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Klenty `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/klenty/latest/actions/get-stepwise-metric-engagements?connectionId=$CONNECTION_ID&cadenceName=Ava%20Chen&endDate=string&startDate=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "cadenceName": "Ava Chen",
  "endDate": "string",
  "startDate": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/klenty/latest/actions/get-stepwise-metric-engagements?${params}`, {
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
| `cadenceName` | string | yes | Cadence name to report stepwise metrics for. |
| `endDate` | string | yes | End date for the engagement window. Use yyyy-mm-dd or an ISO timestamp as documented. |
| `startDate` | string | yes | Start date for the engagement window. Use yyyy-mm-dd or an ISO timestamp as documented. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "callCount": 1,
      "completed": 1,
      "completedCalls": 1,
      "linkCount": 1,
      "linkPercent": 1,
      "mailCount": 1,
      "openCount": 1,
      "openPercent": 1,
      "replyCount": 1,
      "replyPercent": 1,
      "stepNumber": 1,
      "stepType": "string",
      "taskCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `callCount` | number |  |
| `completed` | number |  |
| `completedCalls` | number |  |
| `linkCount` | number |  |
| `linkPercent` | number |  |
| `mailCount` | number |  |
| `openCount` | number |  |
| `openPercent` | number |  |
| `replyCount` | number |  |
| `replyPercent` | number |  |
| `stepNumber` | number |  |
| `stepType` | string |  |
| `taskCount` | number |  |

## Native endpoint

Through the native Klenty API, this operation is `POST /stepWiseEngagements` (base URL `https://api.klenty.com/apis/v1/user/{{credentials.username}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-stepwise-metric-engagements.md) for the provider-specific parameters and requirements.

