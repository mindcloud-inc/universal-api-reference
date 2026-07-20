# BBC Sport - Rugby: List Scotland Rugby Team Headlines

Retrieves Scotland rugby team headlines from BBC Sport - Rugby.

```
GET https://connect.mindcloud.co/v1/universal/bBCSportRugby/latest/actions/list-scotland-rugby-team-headlines
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BBC Sport - Rugby `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bBCSportRugby/latest/actions/list-scotland-rugby-team-headlines?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bBCSportRugby/latest/actions/list-scotland-rugby-team-headlines?${params}`, {
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
      "description": {},
      "guid": "string",
      "link": "https://example.com",
      "pubDate": "2026-05-07T12:00:00.000Z",
      "title": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | object | RSS item description, returned as an XML CDATA object. |
| `guid` | string | RSS GUID for the headline item. |
| `link` | string | Canonical BBC URL for the headline item. |
| `pubDate` | date | RFC 822 publication timestamp for the headline item. |
| `title` | object | RSS item title, returned as an XML CDATA object. |

## Native endpoint

Through the native BBC Sport - Rugby API, this operation is `GET /rugby-union/teams/scotland/rss.xml` (base URL `https://feeds.bbci.co.uk/sport`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-scotland-rugby-team-headlines.md) for the provider-specific parameters and requirements.

