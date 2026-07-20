# Maildrip: Fix and optimize manual email content using AI and analysis report (paid users only)



```
PUT https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/fix-and-optimize-manual-email-content-using-ai-and-analysis-report-paid-users-only
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Maildrip `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/fix-and-optimize-manual-email-content-using-ai-and-analysis-report-paid-users-only" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "type": "string",
  "content": "string",
  "analysis[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/fix-and-optimize-manual-email-content-using-ai-and-analysis-report-paid-users-only', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "type": "string",
    "content": "string",
    "analysis[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `type` | string | yes | Type of content to fix (subject or body) |
| `content` | string | yes | The email subject or body to fix |
| `analysis[]` | array<object> | yes | The analysis report array Accepts multiple values as an array. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "analysisReport": [
        {}
      ],
      "fixedContent": "string",
      "initialContent": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `analysisReport` | array<object> |  |
| `fixedContent` | string | The fixed/optimized content |
| `initialContent` | string | The original content |

## Native endpoint

Through the native Maildrip API, this operation is `POST /api/v1/ai-assistant/fix` (base URL `https://api.maildrip.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/fix-and-optimize-manual-email-content-using-ai-and-analysis-report-paid-users-only.md) for the provider-specific parameters and requirements.

