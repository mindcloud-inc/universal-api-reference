# Cursor: Add Followup



```
POST https://connect.mindcloud.co/v1/universal/cursor/latest/actions/add-followup
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cursor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/cursor/latest/actions/add-followup" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "bc_abc123",
  "prompt.text": "Also add a section about troubleshooting"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cursor/latest/actions/add-followup', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "bc_abc123",
    "prompt.text": "Also add a section about troubleshooting"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Unique identifier for the cloud agent receiving the follow-up. Example: `bc_abc123`. |
| `prompt.text` | string | yes | Follow-up instruction for the agent. Example: `Also add a section about troubleshooting`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `prompt.images[]` | array<object> | no | Optional array of base64 encoded images, maximum 5. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Unique cloud agent identifier. |

## Native endpoint

Through the native Cursor API, this operation is `POST /v0/agents/{{id}}/followup` (base URL `https://api.cursor.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-followup.md) for the provider-specific parameters and requirements.

