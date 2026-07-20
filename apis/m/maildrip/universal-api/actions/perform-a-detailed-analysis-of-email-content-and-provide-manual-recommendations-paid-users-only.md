# Maildrip: Perform a detailed analysis of email content and provide manual recommendations (paid users only)



```
POST https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/perform-a-detailed-analysis-of-email-content-and-provide-manual-recommendations-paid-users-only
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Maildrip `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/perform-a-detailed-analysis-of-email-content-and-provide-manual-recommendations-paid-users-only" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "type": "string",
  "content": "string",
  "audience": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/perform-a-detailed-analysis-of-email-content-and-provide-manual-recommendations-paid-users-only', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "type": "string",
    "content": "string",
    "audience": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `type` | string | yes | Type of content to analyze (subject or body) |
| `content` | string | yes | The email subject or body to analyze |
| `sender` | string | no | The sender persona |
| `audience` | string | yes | The target audience |
| `goal` | string | no | The goal of the email |
| `tone` | string | no | The tone of the email |

## Response

```json
{
  "success": true,
  "data": [
    {
      "analysisReport": {},
      "initialContent": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `analysisReport` | object | The detailed analysis report in JSON format |
| `initialContent` | string | The original content |

## Native endpoint

Through the native Maildrip API, this operation is `POST /api/v1/ai-assistant/detailed-analysis` (base URL `https://api.maildrip.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/perform-a-detailed-analysis-of-email-content-and-provide-manual-recommendations-paid-users-only.md) for the provider-specific parameters and requirements.

