# Fabric: Get Memory

Retrieves a memory from Fabric.

```
GET https://connect.mindcloud.co/v1/universal/fabric/latest/actions/get-memory
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fabric `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fabric/latest/actions/get-memory?connectionId=$CONNECTION_ID&memoryId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "memoryId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fabric/latest/actions/get-memory?${params}`, {
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
| `memoryId` | string | yes | The Fabric memory ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "answer": "string",
      "createdAt": "string",
      "id": "string",
      "modifiedAt": "string",
      "question": "string",
      "status": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `answer` | string |  |
| `createdAt` | string |  |
| `id` | string |  |
| `modifiedAt` | string |  |
| `question` | string |  |
| `status` | string |  |
| `title` | string |  |

## Native endpoint

Through the native Fabric API, this operation is `GET /v2/memories/{memoryId}` (base URL `https://api.fabric.so`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-memory.md) for the provider-specific parameters and requirements.

