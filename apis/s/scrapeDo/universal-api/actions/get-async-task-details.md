# Scrape do: Get async task details

Retrieves async task details from Scrape do.

```
GET https://connect.mindcloud.co/v1/universal/scrapeDo/latest/actions/get-async-task-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Scrape do `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapeDo/latest/actions/get-async-task-details?connectionId=$CONNECTION_ID&jobID=string&taskID=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "jobID": "string",
  "taskID": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scrapeDo/latest/actions/get-async-task-details?${params}`, {
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
| `jobID` | string | yes | The async job identifier. |
| `taskID` | string | yes | The async task identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Base64EncodedContent": true,
      "Content": "string",
      "EndTime": "string",
      "ErrorMessage": "string",
      "ExpiresAt": "string",
      "JobID": "string",
      "ResponseHeaders": {},
      "Scrape": {
        "do": {}
      },
      "StartTime": "string",
      "Status": "string",
      "StatusCode": 1,
      "TaskID": "string",
      "TraceID": "string",
      "UpdateTime": "string",
      "URL": "https://example.com",
      "WebhookRequestTime": "string",
      "WebhookStatus": "string",
      "WebhookURL": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Base64EncodedContent` | boolean | Whether content is base64 encoded. |
| `Content` | string | Task response body. |
| `EndTime` | string | Task end timestamp. |
| `ErrorMessage` | string | Error text when the task fails. |
| `ExpiresAt` | string | Task expiration timestamp when present. |
| `JobID` | string | Parent job identifier. |
| `ResponseHeaders` | object | Response headers from the target. |
| `Scrape.do` | object | Scrape.do metadata for the task. |
| `StartTime` | string | Task start timestamp. |
| `Status` | string | Task status. |
| `StatusCode` | number | HTTP status code from the target. |
| `TaskID` | string | Task identifier. |
| `TraceID` | string | Trace identifier for the task. |
| `UpdateTime` | string | Last task update time when present. |
| `URL` | string | Target URL. |
| `WebhookRequestTime` | string | Webhook request timestamp when configured. |
| `WebhookStatus` | string | Webhook delivery status when configured. |
| `WebhookURL` | string | Webhook destination URL when configured. |

## Native endpoint

Through the native Scrape do API, this operation is `GET https://q.scrape.do/api/v1/jobs/:jobID/:taskID` (base URL `https://api.scrape.do`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-async-task-details.md) for the provider-specific parameters and requirements.

