# Bunnies.io: Get Random Bunny



```
GET https://connect.mindcloud.co/v1/universal/bunniesio/latest/actions/get-random-bunny
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bunnies.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bunniesio/latest/actions/get-random-bunny?connectionId=$CONNECTION_ID&media=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "media": "0"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bunniesio/latest/actions/get-random-bunny?${params}`, {
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
| `media` | list | yes | One or more requested native media formats. Bunnies.io returns matching media URLs plus a poster. One of: `0`, `1`, `2`, `3`. Accepts multiple values in one string, delimited by `,`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "media": {},
      "source": "string",
      "thisServed": 1,
      "totalServed": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Native Bunnies.io bunny identifier. |
| `media` | object | Native media URL object. It preserves selected gif, mp4, av1, or webm URL keys plus poster; no media flattening or URL reconstruction is applied. |
| `source` | string | Provider-supplied original media-source URL or native source marker. |
| `thisServed` | number | Provider current serving counter. |
| `totalServed` | number | Provider total serving counter. |

## Native endpoint

Through the native Bunnies.io API, this operation is `GET /v2/loop/random/` (base URL `https://api.bunnies.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-random-bunny.md) for the provider-specific parameters and requirements.

