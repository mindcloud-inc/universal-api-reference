# Graphor: Ingest URL

Creates a new source in Graphor from a URL.

```
POST https://connect.mindcloud.co/v1/universal/graphor/latest/actions/ingest-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Graphor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/graphor/latest/actions/ingest-url" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/graphor/latest/actions/ingest-url', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "url": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `crawlUrls` | boolean | no | When true, follow and ingest links discovered on the page. |
| `method` | string | no | Optional partition method to use during ingestion. |
| `url` | string | yes | The public web page URL to ingest. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "buildId": "string",
      "error": "string",
      "message": "string",
      "status": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `buildId` | string |  |
| `error` | string |  |
| `message` | string |  |
| `status` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Graphor API, this operation is `POST /ingest-url` (base URL `https://sources.graphorlm.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/ingest-url.md) for the provider-specific parameters and requirements.

