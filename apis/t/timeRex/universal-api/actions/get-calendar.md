# TimeRex: Get Calendar

Retrieves a calendar by ID from TimeRex.

```
GET https://connect.mindcloud.co/v1/universal/timeRex/latest/actions/get-calendar
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TimeRex `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/timeRex/latest/actions/get-calendar?connectionId=$CONNECTION_ID&calendarId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "calendarId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/timeRex/latest/actions/get-calendar?${params}`, {
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
| `calendarId` | string | yes | The TimeRex calendar identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "duration": 1,
      "folderName": {},
      "id": "string",
      "members": [
        {
          "groupNumber": {},
          "id": "string",
          "isSelf": true,
          "name": "Ava Chen"
        }
      ],
      "name": "Ava Chen",
      "onlineMeetingProvider": "string",
      "postTravelTime": 1,
      "preTravelTime": 1,
      "privateName": {},
      "teamId": "string",
      "type": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `duration` | number |  |
| `folderName` | object |  |
| `id` | string |  |
| `members[].groupNumber` | object |  |
| `members[].id` | string |  |
| `members[].isSelf` | boolean |  |
| `members[].name` | string |  |
| `name` | string |  |
| `onlineMeetingProvider` | string |  |
| `postTravelTime` | number |  |
| `preTravelTime` | number |  |
| `privateName` | object |  |
| `teamId` | string |  |
| `type` | string |  |
| `url` | string |  |

## Native endpoint

Through the native TimeRex API, this operation is `GET /calendars/:calendarId` (base URL `https://timerex.net/api/beta`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-calendar.md) for the provider-specific parameters and requirements.

