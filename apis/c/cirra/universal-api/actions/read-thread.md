# Cirra: Get Thread

Retrieves a Cirra thread by thread ID.

```
GET https://connect.mindcloud.co/v1/universal/cirra/latest/actions/read-thread
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cirra `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cirra/latest/actions/read-thread?connectionId=$CONNECTION_ID&threadId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "threadId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cirra/latest/actions/read-thread?${params}`, {
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
| `threadId` | list | yes | The Cirra thread id to read. |
| `advanced` | boolean | no | When true, include advanced thread fields such as composer settings and thread type. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "composerModel": "string",
      "composerReasoningEffort": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "messages": [
        {
          "createdAt": "2026-05-07T12:00:00.000Z",
          "id": "string",
          "role": "string",
          "text": "string"
        }
      ],
      "projectId": "string",
      "status": "string",
      "threadType": "string",
      "title": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `composerModel` | string |  |
| `composerReasoningEffort` | string |  |
| `createdAt` | date |  |
| `id` | string |  |
| `messages[].createdAt` | date |  |
| `messages[].id` | string |  |
| `messages[].role` | string |  |
| `messages[].text` | string |  |
| `projectId` | string |  |
| `status` | string |  |
| `threadType` | string |  |
| `title` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Cirra API, this operation is `GET /v1/cirra/threads/:threadId` (base URL `http://api-public:9801`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/read-thread.md) for the provider-specific parameters and requirements.

