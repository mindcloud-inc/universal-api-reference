# Reka AI: Delete Legacy Video Group

Deletes an existing legacy video group from Reka AI.

```
DELETE https://connect.mindcloud.co/v1/universal/rekaAI/latest/actions/delete-legacy-video-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reka AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/rekaAI/latest/actions/delete-legacy-video-group?connectionId=$CONNECTION_ID&group_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "group_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rekaAI/latest/actions/delete-legacy-video-group?${params}`, {
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
| `group_id` | string | yes | The legacy video group identifier to delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "message": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Deleted identifier. |
| `message` | string | Human-readable message. |
| `success` | boolean | Whether the delete succeeded. |

## Native endpoint

Through the native Reka AI API, this operation is `DELETE https://vision-agent.api.reka.ai/v1/video-groups/:group_id` (base URL `https://api.reka.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-legacy-video-group.md) for the provider-specific parameters and requirements.

