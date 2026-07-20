# LogRocket: Get Highlights Result



```
GET https://connect.mindcloud.co/v1/universal/logRocket/latest/actions/get-highlights-result
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LogRocket `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/logRocket/latest/actions/get-highlights-result?connectionId=$CONNECTION_ID&id=highlights%20request%20id" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "highlights request id"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/logRocket/latest/actions/get-highlights-result?${params}`, {
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
| `id` | string | yes | The highlights request ID returned by Request User Highlights. Example: `highlights request id`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "appID": "string",
      "requestID": "string",
      "result": {
        "highlights": "string",
        "sessions": [
          {
            "highlights": "string",
            "recordingID": "string",
            "sessionID": 1
          }
        ]
      },
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `appID` | string | LogRocket app ID in org/project form |
| `requestID` | string | Highlights request ID |
| `result` | object | Highlights result payload when ready |
| `result.highlights` | string | Markdown summary across included sessions |
| `result.sessions` | array<object> | Per-session highlight summaries |
| `result.sessions[].highlights` | string | Markdown session highlights |
| `result.sessions[].recordingID` | string | LogRocket recording ID |
| `result.sessions[].sessionID` | number | Session ID |
| `status` | string | Generation status such as PENDING, READY, or FAILED |

## Native endpoint

Through the native LogRocket API, this operation is `GET /orgs/:orgId/apps/:projectId/highlights/` (base URL `https://api.logrocket.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-highlights-result.md) for the provider-specific parameters and requirements.

