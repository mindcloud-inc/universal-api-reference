# Langfuse: Update Prompt Version

Updates labels for a Langfuse prompt version.

```
PUT https://connect.mindcloud.co/v1/universal/langfuse/latest/actions/update-prompt-version
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Langfuse `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/langfuse/latest/actions/update-prompt-version" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/langfuse/latest/actions/update-prompt-version', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | no |  |
| `newLabels` | string | no |  |
| `version` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "commitMessage": "string",
      "config": "string",
      "labels": [
        "string"
      ],
      "name": "Ava Chen",
      "resolutionGraph": {},
      "tags": [
        "string"
      ],
      "type": "string",
      "version": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `commitMessage` | string |  |
| `config` | string |  |
| `labels` | array<string> |  |
| `name` | string |  |
| `resolutionGraph` | object |  |
| `tags` | array<string> |  |
| `type` | string |  |
| `version` | number |  |

## Native endpoint

Through the native Langfuse API, this operation is `PATCH /v2/prompts/:name/versions/:version` (base URL `https://cloud.langfuse.com/api/public`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-prompt-version.md) for the provider-specific parameters and requirements.

