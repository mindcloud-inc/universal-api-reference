# Firecrawl: Get Batch Scrape Errors

Retrieves batch scrape errors from Firecrawl.

```
GET https://connect.mindcloud.co/v1/universal/firecrawl/latest/actions/get-batch-scrape-errors
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Firecrawl `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/firecrawl/latest/actions/get-batch-scrape-errors?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/firecrawl/latest/actions/get-batch-scrape-errors?${params}`, {
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
| `id` | string | yes | The ID of the batch scrape job |

## Response

```json
{
  "success": true,
  "data": [
    {
      "errors": [
        {}
      ],
      "robotsBlocked": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `errors` | array<object> |  |
| `robotsBlocked` | array<object> |  |

## Native endpoint

Through the native Firecrawl API, this operation is `GET /batch/scrape/:id/errors` (base URL `https://api.firecrawl.dev/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-batch-scrape-errors.md) for the provider-specific parameters and requirements.

