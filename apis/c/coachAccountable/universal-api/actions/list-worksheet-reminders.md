# CoachAccountable: List Worksheet Reminders

Retrieves worksheet reminders from CoachAccountable.

```
GET https://connect.mindcloud.co/v1/universal/coachAccountable/latest/actions/list-worksheet-reminders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CoachAccountable `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/coachAccountable/latest/actions/list-worksheet-reminders?connectionId=$CONNECTION_ID&worksheetId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "worksheetId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/coachAccountable/latest/actions/list-worksheet-reminders?${params}`, {
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
| `worksheetId` | number | yes |  |
| `includeSent` | boolean | no | Set to true to include Reminders that have already been sent (otherwise just return future reminders, i.e. those yet to be sent. Default: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "dateSent": "2026-05-07T12:00:00.000Z",
      "dateToSend": "2026-05-07T12:00:00.000Z",
      "ID": 1,
      "isSent": true,
      "relativeMinutes": 1,
      "sendMethod": "string",
      "sendTo": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dateSent` | date |  |
| `dateToSend` | date |  |
| `ID` | number |  |
| `isSent` | boolean |  |
| `relativeMinutes` | number |  |
| `sendMethod` | string |  |
| `sendTo` | string |  |

## Native endpoint

Through the native CoachAccountable API, this operation is `POST /` (base URL `https://www.coachaccountable.com/API`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-worksheet-reminders.md) for the provider-specific parameters and requirements.

