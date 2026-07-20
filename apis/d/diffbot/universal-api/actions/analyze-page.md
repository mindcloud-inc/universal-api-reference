# Diffbot: Analyze Page

Analyzes a page and classifies its content with Diffbot.

```
GET https://connect.mindcloud.co/v1/universal/diffbot/latest/actions/analyze-page
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Diffbot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/diffbot/latest/actions/analyze-page?connectionId=$CONNECTION_ID&pageUrl=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "pageUrl": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/diffbot/latest/actions/analyze-page?${params}`, {
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
| `pageUrl` | string | yes | URL to analyze with Diffbot Analyze API. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Diffbot API returns.

## Native endpoint

Through the native Diffbot API, this operation is `GET /v3/analyze` (base URL `https://api.diffbot.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/analyze-page.md) for the provider-specific parameters and requirements.

