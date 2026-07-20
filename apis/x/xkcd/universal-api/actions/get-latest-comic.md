# Xkcd: Get Latest Comic

Retrieves the latest comic metadata from Xkcd.

```
GET https://connect.mindcloud.co/v1/universal/xkcd/latest/actions/get-latest-comic
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Xkcd `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xkcd/latest/actions/get-latest-comic?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xkcd/latest/actions/get-latest-comic?${params}`, {
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
      "alt": "string",
      "day": "string",
      "img": "string",
      "link": "https://example.com",
      "month": "string",
      "news": "string",
      "num": 1,
      "safe_title": "string",
      "title": "string",
      "transcript": "string",
      "year": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `alt` | string | Comic alt text. |
| `day` | string | Publication day of month. |
| `img` | string | Comic image URL. |
| `link` | string | External link associated with the comic, when present. |
| `month` | string | Publication month number. |
| `news` | string | News text associated with the comic, when present. |
| `num` | number | xkcd comic number. |
| `safe_title` | string | Safe title variant from xkcd. |
| `title` | string | Comic title. |
| `transcript` | string | Comic transcript, when available. |
| `year` | string | Publication year. |

## Native endpoint

Through the native Xkcd API, this operation is `GET /info.0.json` (base URL `https://xkcd.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-latest-comic.md) for the provider-specific parameters and requirements.

