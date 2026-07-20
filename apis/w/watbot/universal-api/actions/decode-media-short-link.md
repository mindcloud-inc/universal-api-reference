# Watbot: Decode Media Short Link

Decodes a media short link in Watbot.

```
GET https://connect.mindcloud.co/v1/universal/watbot/latest/actions/decode-media-short-link
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Watbot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/watbot/latest/actions/decode-media-short-link?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fmedia.watbot.short%2Fexample" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://media.watbot.short/example"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/watbot/latest/actions/decode-media-short-link?${params}`, {
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
| `url` | string | yes | Short media URL stored in a Watbot user variable. Example: `https://media.watbot.short/example`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `url` | string | Decoded direct media URL. |

## Native endpoint

Through the native Watbot API, this operation is `POST /decodeShortLink` (base URL `https://watbot.ru/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/decode-media-short-link.md) for the provider-specific parameters and requirements.

