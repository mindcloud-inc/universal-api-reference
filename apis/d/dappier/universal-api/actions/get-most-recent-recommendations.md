# Dappier: Get Most Recent Recommendations

Retrieves the most recent AI article recommendations from Dappier.

```
GET https://connect.mindcloud.co/v1/universal/dappier/latest/actions/get-most-recent-recommendations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dappier `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dappier/latest/actions/get-most-recent-recommendations?connectionId=$CONNECTION_ID&dataModelId=dm_01j1sz8t3qe6v9g8ad102kvmqn&query=dog%20care%20tips" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "dataModelId": "dm_01j1sz8t3qe6v9g8ad102kvmqn",
  "query": "dog care tips"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dappier/latest/actions/get-most-recent-recommendations?${params}`, {
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
| `dataModelId` | string | yes | Data model ID, starting with dm_. Default: `dm_01j1sz8t3qe6v9g8ad102kvmqn`. Example: `dm_01j1sz8t3qe6v9g8ad102kvmqn`. |
| `query` | string | yes | Natural language query, keyword, or URL. Default: `dog care tips`. Example: `dog care tips`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "author": "string",
      "imageUrl": "https://example.com",
      "previewContent": "string",
      "pubdate": "string",
      "pubdateUnix": 1,
      "score": 1,
      "site": "string",
      "siteDomain": "string",
      "sourceUrl": "https://example.com",
      "summary": "string",
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
| `author` | string |  |
| `imageUrl` | string |  |
| `previewContent` | string |  |
| `pubdate` | string |  |
| `pubdateUnix` | number |  |
| `score` | number |  |
| `site` | string |  |
| `siteDomain` | string |  |
| `sourceUrl` | string |  |
| `summary` | string |  |
| `title` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Dappier API, this operation is `POST /app/v2/search` (base URL `https://api.dappier.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-most-recent-recommendations.md) for the provider-specific parameters and requirements.

