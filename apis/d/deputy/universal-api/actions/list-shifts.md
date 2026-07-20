# Deputy: List Shifts

Retrieves the shift list from Deputy.

```
GET https://connect.mindcloud.co/v1/universal/deputy/latest/actions/list-shifts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Deputy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/deputy/latest/actions/list-shifts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/deputy/latest/actions/list-shifts?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



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

Through the native Deputy API, this operation is `POST /api/v1/resource/Roster/QUERY` (base URL `https://{{credentials.endpoint}}.deputy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-shifts.md) for the provider-specific parameters and requirements.

