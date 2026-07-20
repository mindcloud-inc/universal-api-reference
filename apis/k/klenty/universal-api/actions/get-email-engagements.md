# Klenty: Get Email Engagements

Retrieves email engagements from Klenty.

```
GET https://connect.mindcloud.co/v1/universal/klenty/latest/actions/get-email-engagements
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Klenty `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/klenty/latest/actions/get-email-engagements?connectionId=$CONNECTION_ID&cadenceName=Ava%20Chen&endDate=string&startDate=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "cadenceName": "Ava Chen",
  "endDate": "string",
  "startDate": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/klenty/latest/actions/get-email-engagements?${params}`, {
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
| `cadenceName` | string | yes | Cadence name to report email engagement metrics for. |
| `endDate` | string | yes | End date for the engagement window. Use yyyy-mm-dd or an ISO timestamp as documented. |
| `startDate` | string | yes | Start date for the engagement window. Use yyyy-mm-dd or an ISO timestamp as documented. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bounceCount": 1,
      "bounceUiCount": 1,
      "contactedCount": 1,
      "inCadenceCount": 1,
      "linkCount": 1,
      "linkedInTasksReport": {
        "allCount": 1,
        "connectionRequestAccepted": 1,
        "connectionRequestAcceptedPERCENTAGE": "https://example.com",
        "connectionRequestSent": 1,
        "inMailSent": 1,
        "messageResponded": 1,
        "messageSent": 1,
        "responded": 1,
        "respondedPERCENTAGE": "https://example.com"
      },
      "linkUiCount": 1,
      "mailSentCount": 1,
      "openCount": 1,
      "openUiCount": 1,
      "prospectsAdded": 1,
      "prospectsCompleted": 1,
      "replyCount": 1,
      "replyUiCount": 1,
      "unsubscribeCount": 1,
      "unsubscribeUiCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bounceCount` | number |  |
| `bounceUiCount` | number |  |
| `contactedCount` | number |  |
| `inCadenceCount` | number |  |
| `linkCount` | number |  |
| `linkedInTasksReport.allCount` | number |  |
| `linkedInTasksReport.connectionRequestAccepted` | number |  |
| `linkedInTasksReport.connectionRequestAcceptedPERCENTAGE` | string |  |
| `linkedInTasksReport.connectionRequestSent` | number |  |
| `linkedInTasksReport.inMailSent` | number |  |
| `linkedInTasksReport.messageResponded` | number |  |
| `linkedInTasksReport.messageSent` | number |  |
| `linkedInTasksReport.responded` | number |  |
| `linkedInTasksReport.respondedPERCENTAGE` | string |  |
| `linkUiCount` | number |  |
| `mailSentCount` | number |  |
| `openCount` | number |  |
| `openUiCount` | number |  |
| `prospectsAdded` | number |  |
| `prospectsCompleted` | number |  |
| `replyCount` | number |  |
| `replyUiCount` | number |  |
| `unsubscribeCount` | number |  |
| `unsubscribeUiCount` | number |  |

## Native endpoint

Through the native Klenty API, this operation is `POST /emailEngagements` (base URL `https://api.klenty.com/apis/v1/user/{{credentials.username}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-email-engagements.md) for the provider-specific parameters and requirements.

