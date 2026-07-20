# 1minAI: Generate blog article

Creates a blog article in 1minAI.

```
POST https://connect.mindcloud.co/v1/universal/minAI/latest/actions/generate-blog-article
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 1minAI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/minAI/latest/actions/generate-blog-article" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "prompt": "Benefits of solar power"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/minAI/latest/actions/generate-blog-article', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "prompt": "Benefits of solar power"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `prompt` | string | yes | Example: `Benefits of solar power`. |
| `tone` | string | no | Default: `Informative`. |
| `language` | string | no | Default: `English`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `numberOfSection` | number | no |  |
| `numberOfWord` | number | no |  |
| `keywords` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "aiRecord": {},
      "temporaryUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `aiRecord` | object | Generation record. |
| `temporaryUrl` | string | Temporary asset URL when available. |

## Native endpoint

Through the native 1minAI API, this operation is `POST /api/features` (base URL `https://api.1min.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-blog-article.md) for the provider-specific parameters and requirements.

