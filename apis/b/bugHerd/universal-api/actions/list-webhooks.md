# BugHerd: List Webhooks

Retrieves webhooks from BugHerd.

```
GET https://connect.mindcloud.co/v1/universal/bugHerd/latest/actions/list-webhooks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BugHerd `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bugHerd/latest/actions/list-webhooks?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bugHerd/latest/actions/list-webhooks?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "errorCount": 1,
      "event": "string",
      "firstErrorAt": "2026-05-07T12:00:00.000Z",
      "firstSuccessAt": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "lastErrorAt": "2026-05-07T12:00:00.000Z",
      "lastErrorCode": 1,
      "lastSuccessAt": "2026-05-07T12:00:00.000Z",
      "projectId": 1,
      "projectName": "Ava Chen",
      "successCount": 1,
      "targetUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `errorCount` | number | How many failed deliveries BugHerd has recorded. |
| `event` | string | The BugHerd event name. |
| `firstErrorAt` | date | When the first delivery error occurred, when present. |
| `firstSuccessAt` | date | When the first successful delivery occurred, when present. |
| `id` | number | The BugHerd webhook ID. |
| `lastErrorAt` | date | When the last delivery error occurred, when present. |
| `lastErrorCode` | number | The last delivery error code, when present. |
| `lastSuccessAt` | date | When the last successful delivery occurred, when present. |
| `projectId` | number | The BugHerd project ID, when the webhook is project-scoped. |
| `projectName` | string | The BugHerd project name, when the webhook is project-scoped. |
| `successCount` | number | How many successful deliveries BugHerd has recorded. |
| `targetUrl` | string | The webhook target URL. |

## Native endpoint

Through the native BugHerd API, this operation is `GET webhooks.json` (base URL `https://www.bugherd.com/api_v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-webhooks.md) for the provider-specific parameters and requirements.

