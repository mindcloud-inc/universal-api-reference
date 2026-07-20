# Valyu: Create Contents Job



```
POST https://connect.mindcloud.co/v1/universal/valyu/latest/actions/create-contents-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Valyu `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/valyu/latest/actions/create-contents-job" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "urls[]": "Add one or more HTTPS URLs"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/valyu/latest/actions/create-contents-job', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "urls[]": "Add one or more HTTPS URLs"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `urls[]` | array<string> | yes | URLs to extract content from. Example: `Add one or more HTTPS URLs`. |
| `response_length` | string | no | Maximum character length of extracted content per URL. Example: `short, medium, large, max, or a number`. |
| `extract_effort` | string | no | Controls how pages are rendered for extraction. |
| `summary` | string | no | Optional AI-powered content processing mode. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "jobId": "string",
      "pollUrl": "https://example.com",
      "status": "string",
      "success": true,
      "txId": "string",
      "urlsTotal": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `jobId` | string |  |
| `pollUrl` | string |  |
| `status` | string |  |
| `success` | boolean |  |
| `txId` | string |  |
| `urlsTotal` | number |  |

## Native endpoint

Through the native Valyu API, this operation is `POST /contents` (base URL `https://api.valyu.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-contents-job.md) for the provider-specific parameters and requirements.

