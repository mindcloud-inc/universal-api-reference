# LinkupAPI: Get Research Task

Retrieves research task details from LinkupAPI.

```
GET https://connect.mindcloud.co/v1/universal/linkupAPI/latest/actions/get-research-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LinkupAPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/linkupAPI/latest/actions/get-research-task?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/linkupAPI/latest/actions/get-research-task?${params}`, {
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
| `id` | string | yes | The ID of the research task to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "error": "string",
      "id": "string",
      "input": {},
      "output": {},
      "status": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date | When the research task was created. |
| `error` | string | The error message when the research task fails. |
| `id` | string | The research task ID. |
| `input` | object | The input used to create the research task. |
| `output` | object | The output of the research task when completed. |
| `status` | string | The research task status. |
| `updatedAt` | date | When the research task was last updated. |

## Native endpoint

Through the native LinkupAPI API, this operation is `GET /research/:id` (base URL `https://api.linkup.so/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-research-task.md) for the provider-specific parameters and requirements.

