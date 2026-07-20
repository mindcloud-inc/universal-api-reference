# Xkcd: Get Comic

Retrieves comic metadata from Xkcd by comic number.

```
GET https://connect.mindcloud.co/v1/universal/xkcd/latest/actions/get-comic
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Xkcd `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xkcd/latest/actions/get-comic?connectionId=$CONNECTION_ID&comicNumber=614" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "comicNumber": "614"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xkcd/latest/actions/get-comic?${params}`, {
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
| `comicNumber` | number | yes | The xkcd comic number to fetch, as documented in the /614/info.0.json example. Example: `614`. |

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

Through the native Xkcd API, this operation is `GET /:comicNumber/info.0.json` (base URL `https://xkcd.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-comic.md) for the provider-specific parameters and requirements.

