# Langfuse: Get Prompt

Retrieves a prompt from Langfuse.

```
GET https://connect.mindcloud.co/v1/universal/langfuse/latest/actions/get-prompt
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Langfuse `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/langfuse/latest/actions/get-prompt?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/langfuse/latest/actions/get-prompt?${params}`, {
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
| `label` | string | no |  |
| `promptName` | string | no |  |
| `resolve` | string | no |  |
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

Through the native Langfuse API, this operation is `GET /v2/prompts/:promptName` (base URL `https://cloud.langfuse.com/api/public`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-prompt.md) for the provider-specific parameters and requirements.

