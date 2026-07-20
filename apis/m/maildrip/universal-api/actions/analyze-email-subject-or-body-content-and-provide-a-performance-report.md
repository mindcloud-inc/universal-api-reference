# Maildrip: Analyze email subject or body content and provide a performance report



```
GET https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/analyze-email-subject-or-body-content-and-provide-a-performance-report
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Maildrip `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/analyze-email-subject-or-body-content-and-provide-a-performance-report?connectionId=$CONNECTION_ID&type=string&content=string&audience=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "type": "string",
  "content": "string",
  "audience": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/analyze-email-subject-or-body-content-and-provide-a-performance-report?${params}`, {
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
      "initialRequest": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `analysisReport` | object | The analysis report in JSON format |
| `initialRequest` | object | The initial request data |

## Native endpoint

Through the native Maildrip API, this operation is `POST /api/v1/ai-assistant/analyze` (base URL `https://api.maildrip.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/analyze-email-subject-or-body-content-and-provide-a-performance-report.md) for the provider-specific parameters and requirements.

