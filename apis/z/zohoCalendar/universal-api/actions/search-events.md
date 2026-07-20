# Zoho Calendar: Search Events

Finds events in a Zoho Calendar calendar.

```
GET https://connect.mindcloud.co/v1/universal/zohoCalendar/latest/actions/search-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Calendar `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoCalendar/latest/actions/search-events?connectionId=$CONNECTION_ID&calendarUid=string&searchText=string&start=string&end=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "calendarUid": "string",
  "searchText": "string",
  "start": "string",
  "end": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoCalendar/latest/actions/search-events?${params}`, {
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
| `calendarUid` | string | yes | Calendar unique identifier to search within. |
| `searchText` | string | yes | Text to search for in event titles. |
| `start` | string | yes | Search start datetime in yyyyMMdd'T'HHmmss'Z' format. |
| `end` | string | yes | Search end datetime in yyyyMMdd'T'HHmmss'Z' format. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "haspagination": true,
      "search": [
        {
          "caluid": "string",
          "dateandtime": {
            "end": "string",
            "start": "string",
            "timezone": "string"
          },
          "description": "string",
          "enddate": "string",
          "isApproved": true,
          "location": "string",
          "organizer": "string",
          "startdate": "string",
          "title": "string",
          "uid": "string"
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
| `haspagination` | boolean |  |
| `search[].caluid` | string |  |
| `search[].dateandtime.end` | string |  |
| `search[].dateandtime.start` | string |  |
| `search[].dateandtime.timezone` | string |  |
| `search[].description` | string |  |
| `search[].enddate` | string |  |
| `search[].isApproved` | boolean |  |
| `search[].location` | string |  |
| `search[].organizer` | string |  |
| `search[].startdate` | string |  |
| `search[].title` | string |  |
| `search[].uid` | string |  |

## Native endpoint

Through the native Zoho Calendar API, this operation is `GET /calendars/:calendaruid/search` (base URL `https://calendar.zoho.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-events.md) for the provider-specific parameters and requirements.

