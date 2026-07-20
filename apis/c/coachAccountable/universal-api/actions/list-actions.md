# CoachAccountable: List Actions

Retrieves actions from CoachAccountable.

```
GET https://connect.mindcloud.co/v1/universal/coachAccountable/latest/actions/list-actions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CoachAccountable `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/coachAccountable/latest/actions/list-actions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/coachAccountable/latest/actions/list-actions?${params}`, {
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
| `clientId` | number | no | Filter Actions by Client. |
| `actionProjectId` | number | no | Filter the Actions you get back down to a given project. |
| `projectName` | string | no | Filter the Actions you get back by project name. Supports partial matches on prefix. |
| `includeDone` | boolean | no | Set to true to include Actions that have already been marked complete. Default: `false`. |
| `includeCanceled` | boolean | no | Set to true to include Actions that have been canceled. Default: `false`. |
| `includeForCoach` | boolean | no | Set to true to include Actions that are for the coach to do. Default: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "action": "string",
      "ActionProjectID": 1,
      "ClientID": 1,
      "CoachID": 1,
      "dateDone": "2026-05-07T12:00:00.000Z",
      "dateDue": "2026-05-07T12:00:00.000Z",
      "forWho": "string",
      "ID": 1,
      "isCanceled": true,
      "isDone": true,
      "projectName": "Ava Chen",
      "reminderSet": [
        {
          "dateSent": "2026-05-07T12:00:00.000Z",
          "dateToSend": "2026-05-07T12:00:00.000Z",
          "ID": 1,
          "isSent": true,
          "relativeMinutes": 1,
          "sendMethod": "string",
          "sendTo": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `action` | string |  |
| `ActionProjectID` | number |  |
| `ClientID` | number |  |
| `CoachID` | number |  |
| `dateDone` | date |  |
| `dateDue` | date |  |
| `forWho` | string |  |
| `ID` | number |  |
| `isCanceled` | boolean |  |
| `isDone` | boolean |  |
| `projectName` | string |  |
| `reminderSet` | array<object> |  |
| `reminderSet[].dateSent` | date |  |
| `reminderSet[].dateToSend` | date |  |
| `reminderSet[].ID` | number |  |
| `reminderSet[].isSent` | boolean |  |
| `reminderSet[].relativeMinutes` | number |  |
| `reminderSet[].sendMethod` | string |  |
| `reminderSet[].sendTo` | string |  |

## Native endpoint

Through the native CoachAccountable API, this operation is `POST /` (base URL `https://www.coachaccountable.com/API`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-actions.md) for the provider-specific parameters and requirements.

