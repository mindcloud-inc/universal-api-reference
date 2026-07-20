# Deputy: Add Shift

Creates a new shift in Deputy.

```
POST https://connect.mindcloud.co/v1/universal/deputy/latest/actions/add-shift
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Deputy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/deputy/latest/actions/add-shift" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/deputy/latest/actions/add-shift', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `intStartTimestamp` | number | no | Start time of the shift in unix timestamp format. |
| `intEndTimestamp` | number | no | End time of the shift in unix timestamp format. |
| `intRosterEmployee` | number | no | Id of the employee working the shift when the shift is filled. |
| `blnPublish` | boolean | no | Whether the shift should be published. |
| `intMealbreakMinute` | number | no | Number of minutes to include as a meal break. |
| `intOpunitId` | number | no | The location or area id for the shift. |
| `blnForceOverwrite` | number | no | Whether to force overwrite with 0 or 1. |
| `blnOpen` | number | no | Whether the shift is open using 0 or 1. |
| `strComment` | string | no | Comment text on the shift. |
| `intConfirmStatus` | number | no | Whether the employee's shift should be confirmed with 1 or 0. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_DPMetaData": {},
      "Comment": "string",
      "ConfirmStatus": 1,
      "Created": "2026-05-07T12:00:00.000Z",
      "Date": "2026-05-07T12:00:00.000Z",
      "Employee": 1,
      "EndTime": 1,
      "EndTimeLocalized": "2026-05-07T12:00:00.000Z",
      "Id": 1,
      "Mealbreak": "2026-05-07T12:00:00.000Z",
      "Modified": "2026-05-07T12:00:00.000Z",
      "OperationalUnit": 1,
      "Published": true,
      "Slots": [
        {}
      ],
      "StartTime": 1,
      "StartTimeLocalized": "2026-05-07T12:00:00.000Z",
      "TotalTime": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_DPMetaData` | object |  |
| `Comment` | string |  |
| `ConfirmStatus` | number |  |
| `Created` | date |  |
| `Date` | date |  |
| `Employee` | number |  |
| `EndTime` | number |  |
| `EndTimeLocalized` | date |  |
| `Id` | number |  |
| `Mealbreak` | date |  |
| `Modified` | date |  |
| `OperationalUnit` | number |  |
| `Published` | boolean |  |
| `Slots` | array<object> |  |
| `StartTime` | number |  |
| `StartTimeLocalized` | date |  |
| `TotalTime` | number |  |

## Native endpoint

Through the native Deputy API, this operation is `POST /api/v1/supervise/roster` (base URL `https://{{credentials.endpoint}}.deputy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-shift.md) for the provider-specific parameters and requirements.

