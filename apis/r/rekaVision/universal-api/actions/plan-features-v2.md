# Reka Vision: Plan Features (V2)

Retrieves feature planning results from Reka Vision.

```
GET https://connect.mindcloud.co/v1/universal/rekaVision/latest/actions/plan-features-v2
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reka Vision `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rekaVision/latest/actions/plan-features-v2?connectionId=$CONNECTION_ID&videoId=string&desired%5B%5D=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "videoId": "string",
  "desired[]": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rekaVision/latest/actions/plan-features-v2?${params}`, {
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
| `videoId` | string | yes |  |
| `desired[]` | array<string> | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "actionable": [
        "string"
      ],
      "allRequired": [
        "string"
      ],
      "blocked": [
        "string"
      ],
      "done": true,
      "errors": {},
      "processing": [
        "string"
      ],
      "reconfigure": {},
      "statuses": {},
      "videoId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `actionable` | array<string> |  |
| `allRequired` | array<string> |  |
| `blocked` | array<string> |  |
| `done` | boolean |  |
| `errors` | object |  |
| `processing` | array<string> |  |
| `reconfigure` | object |  |
| `statuses` | object |  |
| `videoId` | string |  |

## Native endpoint

Through the native Reka Vision API, this operation is `POST /v2/videos/:videoId/features/plan` (base URL `https://vision-agent.api.reka.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/plan-features-v2.md) for the provider-specific parameters and requirements.

