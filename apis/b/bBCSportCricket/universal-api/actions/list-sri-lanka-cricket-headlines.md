# BBC Sport - Cricket: List Sri Lanka Cricket Headlines

Retrieves BBC Sport Sri Lanka cricket headlines.

```
GET https://connect.mindcloud.co/v1/universal/bBCSportCricket/latest/actions/list-sri-lanka-cricket-headlines
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BBC Sport - Cricket `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bBCSportCricket/latest/actions/list-sri-lanka-cricket-headlines?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bBCSportCricket/latest/actions/list-sri-lanka-cricket-headlines?${params}`, {
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
      "id": "string",
      "publishedAt": "2026-05-07T12:00:00.000Z",
      "title": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string | BBC summary or standfirst. |
| `id` | string | Stable BBC item identifier. |
| `publishedAt` | date | Publication timestamp when present. |
| `title` | string | BBC headline title. |
| `url` | string | Canonical BBC article or media URL. |

## Native endpoint

Through the native BBC Sport - Cricket API, this operation is `GET /sport/cricket/teams/sri-lanka/rss.xml` (base URL `https://feeds.bbci.co.uk`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-sri-lanka-cricket-headlines.md) for the provider-specific parameters and requirements.

