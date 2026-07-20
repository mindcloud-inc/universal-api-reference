# Xkcd: Get Atom Feed

Retrieves the Atom comic feed from Xkcd.

```
GET https://connect.mindcloud.co/v1/universal/xkcd/latest/actions/get-atom-feed
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Xkcd `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xkcd/latest/actions/get-atom-feed?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xkcd/latest/actions/get-atom-feed?${params}`, {
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
      "entry": [
        {}
      ],
      "id": "string",
      "link": "https://example.com",
      "summary": "string",
      "title": "string",
      "updated": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `entry` | array<object> | Atom comic feed entries. |
| `id` | string | Atom feed or entry stable identifier. |
| `link` | string | Atom feed or entry link. |
| `summary` | string | Atom entry HTML summary. |
| `title` | string | Atom feed or entry title. |
| `updated` | string | Atom feed or entry updated timestamp. |

## Native endpoint

Through the native Xkcd API, this operation is `GET /atom.xml` (base URL `https://xkcd.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-atom-feed.md) for the provider-specific parameters and requirements.

