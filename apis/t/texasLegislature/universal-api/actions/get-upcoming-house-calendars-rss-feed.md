# Texas Legislature: Get Upcoming House Calendars RSS Feed

Retrieves upcoming House calendars from Texas Legislature.

```
GET https://connect.mindcloud.co/v1/universal/texasLegislature/latest/actions/get-upcoming-house-calendars-rss-feed
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Texas Legislature `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/texasLegislature/latest/actions/get-upcoming-house-calendars-rss-feed?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/texasLegislature/latest/actions/get-upcoming-house-calendars-rss-feed?${params}`, {
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
      "description": "string",
      "guid": "string",
      "link": "https://example.com",
      "pubDate": "2026-05-07T12:00:00.000Z",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string | RSS item summary or description. |
| `guid` | string | RSS item GUID. |
| `link` | string | URL linked by the RSS item. |
| `pubDate` | date | RSS item publication date when present. |
| `title` | string | RSS item title. |

## Native endpoint

Through the native Texas Legislature API, this operation is `GET /MyTLO/RSS/RSS.aspx?Type=upcomingcalendarshouse` (base URL `https://capitol.texas.gov`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-upcoming-house-calendars-rss-feed.md) for the provider-specific parameters and requirements.

