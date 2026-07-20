# Deepgram: Get Project Request

Retrieves a project request from Deepgram.

```
GET https://connect.mindcloud.co/v1/universal/deepgram/latest/actions/get-project-request
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Deepgram `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/deepgram/latest/actions/get-project-request?connectionId=$CONNECTION_ID&projectId=string&requestId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "string",
  "requestId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/deepgram/latest/actions/get-project-request?${params}`, {
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
| `requestId` | string | yes | Deepgram request identifier. |

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

Through the native Deepgram API, this operation is `GET /v1/projects/:project_id/requests/:request_id` (base URL `https://api.deepgram.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project-request.md) for the provider-specific parameters and requirements.

