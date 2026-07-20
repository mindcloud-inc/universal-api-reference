# Hyperbrowser: Search the Web



```
GET https://connect.mindcloud.co/v1/universal/hyperbrowser/latest/actions/search-the-web
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hyperbrowser `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hyperbrowser/latest/actions/search-the-web?connectionId=$CONNECTION_ID&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hyperbrowser/latest/actions/search-the-web?${params}`, {
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
| `query` | string | yes | Search query to run. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "jobId": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Search payload, including the query and result list. |
| `jobId` | string | Search job identifier. |
| `status` | string | Job completion status. |

## Native endpoint

Through the native Hyperbrowser API, this operation is `POST /api/web/search` (base URL `https://api.hyperbrowser.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-the-web.md) for the provider-specific parameters and requirements.

