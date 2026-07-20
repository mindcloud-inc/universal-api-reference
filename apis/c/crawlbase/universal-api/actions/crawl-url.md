# Crawlbase: Crawl URL

Retrieves a crawled page from Crawlbase.

```
GET https://connect.mindcloud.co/v1/universal/crawlbase/latest/actions/crawl-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Crawlbase `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/crawlbase/latest/actions/crawl-url?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/crawlbase/latest/actions/crawl-url?${params}`, {
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
| `url` | string | yes | Fully qualified URL to crawl. Crawlbase requires it to start with http or https. Example: `https://example.com`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "body": "string",
      "original_status": 1,
      "pc_status": 1,
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `body` | string | Crawled response body when using JSON format. |
| `original_status` | number | HTTP status Crawlbase received from the target URL. |
| `pc_status` | number | Crawlbase processing status code. |
| `url` | string | Original or followed URL. |

## Native endpoint

Through the native Crawlbase API, this operation is `GET /` (base URL `https://api.crawlbase.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/crawl-url.md) for the provider-specific parameters and requirements.

