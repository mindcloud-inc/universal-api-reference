# TLY Link Shortener: Delete OneLink Stats

Deletes stats for a OneLink in TLY Link Shortener.

```
DELETE https://connect.mindcloud.co/v1/universal/tLYLinkShortener/latest/actions/delete-one-link-stats
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TLY Link Shortener `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/tLYLinkShortener/latest/actions/delete-one-link-stats?connectionId=$CONNECTION_ID&shortUrl=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "shortUrl": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tLYLinkShortener/latest/actions/delete-one-link-stats?${params}`, {
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
| `shortUrl` | string | yes | The OneLink short URL whose stats should be deleted. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "response": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response` | string |  |

## Native endpoint

Through the native TLY Link Shortener API, this operation is `DELETE /api/v1/onelink/stat` (base URL `https://api.t.ly`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-one-link-stats.md) for the provider-specific parameters and requirements.

