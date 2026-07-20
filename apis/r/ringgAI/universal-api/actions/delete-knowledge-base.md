# Ringg AI: Delete Knowledge Base

Deletes a knowledge base from Ringg AI.

```
DELETE https://connect.mindcloud.co/v1/universal/ringgAI/latest/actions/delete-knowledge-base
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ringg AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/ringgAI/latest/actions/delete-knowledge-base?connectionId=$CONNECTION_ID&kbId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "kbId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ringgAI/latest/actions/delete-knowledge-base?${params}`, {
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
| `kbId` | string | yes | (Required) ID of the knowledge base to delete |

## Response

```json
{
  "success": true,
  "data": [
    {
      "kbId": "string",
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `kbId` | string |  |
| `message` | string |  |

## Native endpoint

Through the native Ringg AI API, this operation is `DELETE /external/kb/:kb_id` (base URL `https://prod-api.ringg.ai/ca/api/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-knowledge-base.md) for the provider-specific parameters and requirements.

