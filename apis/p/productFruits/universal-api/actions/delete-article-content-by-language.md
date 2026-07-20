# Product Fruits: Delete Article Content by Language



```
DELETE https://connect.mindcloud.co/v1/universal/productFruits/latest/actions/delete-article-content-by-language
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Product Fruits `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/productFruits/latest/actions/delete-article-content-by-language?connectionId=$CONNECTION_ID&correlationId=string&lang=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "correlationId": "string",
  "lang": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/productFruits/latest/actions/delete-article-content-by-language?${params}`, {
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
| `correlationId` | string | yes | The correlation ID of the article whose language content will be deleted. |
| `lang` | string | yes | ISO 639-1 language code of the content to delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |

## Native endpoint

Through the native Product Fruits API, this operation is `DELETE /v1/knowledgebase/articles/:correlationId/content/:lang` (base URL `https://api.productfruits.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-article-content-by-language.md) for the provider-specific parameters and requirements.

