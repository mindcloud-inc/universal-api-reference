# CometAPI: Midjourney Get Task

Retrieves a Midjourney task from CometAPI.

```
GET https://connect.mindcloud.co/v1/universal/cometAPI/latest/actions/midjourney-get-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CometAPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cometAPI/latest/actions/midjourney-get-task?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cometAPI/latest/actions/midjourney-get-task?${params}`, {
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
| `id` | string | yes | Task identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "imageUrl": "https://example.com",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `imageUrl` | string |  |
| `status` | string |  |

## Native endpoint

Through the native CometAPI API, this operation is `GET /mj/task/:id/fetch` (base URL `https://api.cometapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/midjourney-get-task.md) for the provider-specific parameters and requirements.

