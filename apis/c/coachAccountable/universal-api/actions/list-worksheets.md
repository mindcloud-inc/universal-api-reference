# CoachAccountable: List Worksheets

Retrieves worksheets from CoachAccountable.

```
GET https://connect.mindcloud.co/v1/universal/coachAccountable/latest/actions/list-worksheets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CoachAccountable `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/coachAccountable/latest/actions/list-worksheets?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/coachAccountable/latest/actions/list-worksheets?${params}`, {
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
| `clientId` | number | no | Filter Worksheets by Client. |
| `companyId` | number | no | Filter Client Worksheets by which Company they belong to. |
| `title` | string | no | Filter a Client's Worksheets by which title, prefixed. |
| `includeContent` | boolean | no | Set to true to include the full HTML content of the Worksheet. Default: `false`. |
| `includeOutstanding` | boolean | no | Set to true to include Worksheets not yet marked complete. Default: `false`. |
| `dateAssignedFrom` | date | no | Set to filter Worksheet by when they were assigned. |
| `dateAssignedTo` | date | no | Set to filter Worksheet by when they were assigned. |
| `sortField` | list | no | One of: `dateAssigned`, `dateDone`, `dateDue`. Default: `dateAssigned`. |
| `sortDirection` | list | no | One of: `A`, `D`. Default: `D`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "answerSet": [
        {
          "name": "Ava Chen",
          "numberValue": 1,
          "value": "string"
        }
      ],
      "ClientID": 1,
      "CoachID": 1,
      "content": "string",
      "dateAssigned": "2026-05-07T12:00:00.000Z",
      "dateDone": "2026-05-07T12:00:00.000Z",
      "dateDue": "2026-05-07T12:00:00.000Z",
      "ID": 1,
      "isDone": true,
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
      ],
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `answerSet` | array<object> |  |
| `answerSet[].name` | string |  |
| `answerSet[].numberValue` | number |  |
| `answerSet[].value` | string |  |
| `ClientID` | number |  |
| `CoachID` | number |  |
| `content` | string |  |
| `dateAssigned` | date |  |
| `dateDone` | date |  |
| `dateDue` | date |  |
| `ID` | number |  |
| `isDone` | boolean |  |
| `reminderSet` | array<object> |  |
| `reminderSet[].dateSent` | date |  |
| `reminderSet[].dateToSend` | date |  |
| `reminderSet[].ID` | number |  |
| `reminderSet[].isSent` | boolean |  |
| `reminderSet[].relativeMinutes` | number |  |
| `reminderSet[].sendMethod` | string |  |
| `reminderSet[].sendTo` | string |  |
| `title` | string |  |

## Native endpoint

Through the native CoachAccountable API, this operation is `POST /` (base URL `https://www.coachaccountable.com/API`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-worksheets.md) for the provider-specific parameters and requirements.

