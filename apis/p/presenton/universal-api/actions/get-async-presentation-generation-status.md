# Presenton: Get Async Presentation Generation Status



```
GET https://connect.mindcloud.co/v1/universal/presenton/latest/actions/get-async-presentation-generation-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Presenton `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/presenton/latest/actions/get-async-presentation-generation-status?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/presenton/latest/actions/get-async-presentation-generation-status?${params}`, {
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
| `id` | string | yes | The async task ID to check. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "data": {
        "creditsConsumed": 1,
        "editPath": "string",
        "path": "string",
        "presentationId": "string"
      },
      "id": "string",
      "message": "string",
      "status": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string |  |
| `data.creditsConsumed` | number |  |
| `data.editPath` | string |  |
| `data.path` | string |  |
| `data.presentationId` | string |  |
| `id` | string |  |
| `message` | string |  |
| `status` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Presenton API, this operation is `GET /api/v1/ppt/presentation/status/:id` (base URL `https://api.presenton.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-async-presentation-generation-status.md) for the provider-specific parameters and requirements.

