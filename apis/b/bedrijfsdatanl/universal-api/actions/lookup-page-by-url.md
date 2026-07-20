# Bedrijfsdata.nl: Lookup Page By URL



```
GET https://connect.mindcloud.co/v1/universal/bedrijfsdatanl/latest/actions/lookup-page-by-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bedrijfsdata.nl `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bedrijfsdatanl/latest/actions/lookup-page-by-url?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bedrijfsdatanl/latest/actions/lookup-page-by-url?${params}`, {
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
| `url` | string | no | URL to analyze with RAG. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "articleSource": "string",
      "content": "string",
      "creditsUsed": 1,
      "creditsUsedMonth": 1,
      "description": "string",
      "lang": "string",
      "monthlyCredits": 1,
      "product": "string",
      "status": "string",
      "title": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `articleSource` | string |  |
| `content` | string |  |
| `creditsUsed` | number |  |
| `creditsUsedMonth` | number |  |
| `description` | string |  |
| `lang` | string |  |
| `monthlyCredits` | number |  |
| `product` | string |  |
| `status` | string |  |
| `title` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Bedrijfsdata.nl API, this operation is `GET /rag_url` (base URL `https://fapi.bedrijfsdata.nl/v1.2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/lookup-page-by-url.md) for the provider-specific parameters and requirements.

