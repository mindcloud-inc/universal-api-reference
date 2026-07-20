# Deepgram: List Project Requests

Retrieves project requests from Deepgram.

```
GET https://connect.mindcloud.co/v1/universal/deepgram/latest/actions/list-project-requests
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Deepgram `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/deepgram/latest/actions/list-project-requests?connectionId=$CONNECTION_ID&projectId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/deepgram/latest/actions/list-project-requests?${params}`, {
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
| `projectId` | string | yes | Deepgram project identifier. |
| `start` | string | no | Start of the requested date range in YYYY-MM-DD or ISO date-time format. |
| `end` | string | no | End of the requested date range in YYYY-MM-DD or ISO date-time format. |
| `accessor` | string | no | Filter request logs by accessor identifier. |
| `deployment` | string | no | Filter request logs by deployment: hosted, beta, or self-hosted. |
| `endpoint` | string | no | Filter request logs by endpoint: listen, read, speak, or agent. |
| `method` | string | no | Filter request logs by method: sync, async, or streaming. |
| `status` | string | no | Filter request logs by status: succeeded or failed. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "apiKeyId": "string",
      "callback": "string",
      "created": "string",
      "path": "string",
      "projectUuid": "string",
      "requestId": "string",
      "response": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `apiKeyId` | string |  |
| `callback` | string |  |
| `created` | string |  |
| `path` | string |  |
| `projectUuid` | string |  |
| `requestId` | string |  |
| `response` | object |  |

## Native endpoint

Through the native Deepgram API, this operation is `GET /v1/projects/:project_id/requests` (base URL `https://api.deepgram.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-project-requests.md) for the provider-specific parameters and requirements.

