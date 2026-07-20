# CoachAccountable: Create Action

Creates an action in CoachAccountable.

```
POST https://connect.mindcloud.co/v1/universal/coachAccountable/latest/actions/create-action
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CoachAccountable `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/coachAccountable/latest/actions/create-action" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "clientId": 1,
  "theAction": "string",
  "dateDue": "2026-05-07T12:00:00.000Z",
  "timeDue": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/coachAccountable/latest/actions/create-action', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "clientId": 1,
    "theAction": "string",
    "dateDue": "2026-05-07T12:00:00.000Z",
    "timeDue": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `clientId` | number | yes | ID of the Client to whom this Action is to be assigned. |
| `theAction` | string | yes | A one-liner text of "what" the Action is. |
| `dateDue` | date | yes | Date on which the Action is to be done. |
| `timeDue` | string | yes | Time of day by which the Action is to be done. |
| `timezoneOf` | list | no | Who's timezone the due date is in. Defaults to that of the assigning Coach. One of: `A`, `C`, `L`. |
| `comment` | string | no | An optional additional comment about this Action. |
| `sendNotification` | boolean | no | Send true to notify the client via email of this new Action. Default: `false`. |
| `projectName` | string | no | Name of the Project for the new Action to be filed under. If left blank the new Action will be a standalone one. |
| `actionProjectId` | number | no | An alternative to projectName for specifying which project the new Action should be filed under. |
| `weight` | number | no | Integer describing the relative significance of the Action within a project. Relevant only to Actions that are added to a project. |
| `isLocked` | boolean | no | Prevent the Client from modifying or deleting the Action. Default: `false`. |
| `reminderSet` | string | no | A semi-colon-separated list of comma-separated triplets, each defining a reminder. In a triplet, the first value defines who to send it to ([C]oach or c[L]ient),the second value defines the send method ([E]mail or [T]ext), and the third value defines when to send the reminder, as minutes relative to the due date. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ActionID": 1,
      "ActionProjectID": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ActionID` | number |  |
| `ActionProjectID` | number |  |

## Native endpoint

Through the native CoachAccountable API, this operation is `POST /` (base URL `https://www.coachaccountable.com/API`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-action.md) for the provider-specific parameters and requirements.

