# You.com: Get Contents

Retrieves page contents from You.com.

```
GET https://connect.mindcloud.co/v1/universal/youcom/latest/actions/get-contents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a You.com `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/youcom/latest/actions/get-contents?connectionId=$CONNECTION_ID&urls%5B%5D=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "urls[]": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/youcom/latest/actions/get-contents?${params}`, {
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
| `urls[]` | array<string> | yes | URLs to fetch. |
| `formats[]` | array<string> | no | Content formats to return. |
| `crawlTimeout` | number | no | Live crawl timeout in seconds. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "markdown": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `markdown` | string | Extracted markdown content for the fetched URL. |
| `url` | string | Source URL that was fetched. |

## Native endpoint

Through the native You.com API, this operation is `POST https://ydc-index.io/v1/contents` (base URL `https://api.you.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contents.md) for the provider-specific parameters and requirements.

