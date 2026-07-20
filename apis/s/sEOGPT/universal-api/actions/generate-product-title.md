# SEO GPT: Generate Product Title



```
GET https://connect.mindcloud.co/v1/universal/sEOGPT/latest/actions/generate-product-title
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SEO GPT `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sEOGPT/latest/actions/generate-product-title?connectionId=$CONNECTION_ID&kw=best%20running%20shoes" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "kw": "best running shoes"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sEOGPT/latest/actions/generate-product-title?${params}`, {
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
| `kw` | string | yes | Keyword or phrase to use for the generated copy. Example: `best running shoes`. |
| `web` | string | no | Optional page URL to analyze before generating the copy. Example: `https://example.com/products/running-shoes`. |
| `brand` | string | no | Optional brand name to include in the generated copy. Example: `Example Brand`. |

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
| `response` | string | Generated SEO GPT copy returned as plain text. |

## Native endpoint

Through the native SEO GPT API, this operation is `GET /gpt-get-chrome.php` (base URL `https://ai.seovendor.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-product-title.md) for the provider-specific parameters and requirements.

