# TimeRex Universal API Examples

These examples use the MindCloud API key and TimeRex connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Calendar

Retrieves a calendar by ID from TimeRex.

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

Example response:

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

See the full [Get Calendar action reference](actions/get-calendar.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/timeRex/latest/actions/get-calendar).
