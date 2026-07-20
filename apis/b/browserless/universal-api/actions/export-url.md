# Browserless: Export Url

Downloads a URL in its native format from Browserless.

```
GET https://connect.mindcloud.co/v1/universal/browserless/latest/actions/export-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Browserless `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/browserless/latest/actions/export-url?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/browserless/latest/actions/export-url?${params}`, {
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
| `url` | string | yes | The URL to export in its native content type. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `includeResources` | boolean | no | Whether to return a ZIP archive with the page HTML and linked resources. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Browserless API returns.

## Native endpoint

Through the native Browserless API, this operation is `POST /export` (base URL `https://production-sfo.browserless.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/export-url.md) for the provider-specific parameters and requirements.

