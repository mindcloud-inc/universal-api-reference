# LLMWhisperer: Get Usage Stats

Retrieves tagged usage statistics from LLMWhisperer.

```
GET https://connect.mindcloud.co/v1/universal/lLMWhisperer/latest/actions/get-usage-stats
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LLMWhisperer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lLMWhisperer/latest/actions/get-usage-stats?connectionId=$CONNECTION_ID&tag=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "tag": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lLMWhisperer/latest/actions/get-usage-stats?${params}`, {
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
| `tag` | string | yes | Tag to filter usage statistics. |
| `fromDate` | date | no | Start date in YYYY-MM-DD format. |
| `toDate` | date | no | End date in YYYY-MM-DD format. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "end_date": "string",
      "start_date": "string",
      "subscription_id": "string",
      "tag": "string",
      "usage": [
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
| `end_date` | string |  |
| `start_date` | string |  |
| `subscription_id` | string |  |
| `tag` | string |  |
| `usage` | array<object> |  |

## Native endpoint

Through the native LLMWhisperer API, this operation is `GET /usage` (base URL `https://llmwhisperer-api.us-central.unstract.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-usage-stats.md) for the provider-specific parameters and requirements.

