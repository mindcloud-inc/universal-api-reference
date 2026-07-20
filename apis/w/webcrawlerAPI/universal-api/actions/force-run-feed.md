# Webcrawler API: Force Run Feed

Triggers an immediate feed run in Webcrawler API.

```
PUT https://connect.mindcloud.co/v1/universal/webcrawlerAPI/latest/actions/force-run-feed
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Webcrawler API `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/webcrawlerAPI/latest/actions/force-run-feed" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/webcrawlerAPI/latest/actions/force-run-feed', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Feed identifier to run immediately. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "jobId": "string",
      "message": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Triggered feed run identifier. |
| `jobId` | string | Associated crawl job identifier for the forced run. |
| `message` | string | Provider force-run confirmation message. |
| `status` | string | Current forced-run status returned by the provider. |

## Native endpoint

Through the native Webcrawler API API, this operation is `PUT /v2/feed/:id/run` (base URL `https://api.webcrawlerapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/force-run-feed.md) for the provider-specific parameters and requirements.

