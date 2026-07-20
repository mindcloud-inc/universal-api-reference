# Arize AX: Create a Prompt

Creates a new prompt in Arize AX.

```
POST https://connect.mindcloud.co/v1/universal/arizeAX/latest/actions/create-a-prompt
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Arize AX `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/arizeAX/latest/actions/create-a-prompt" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "version": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/arizeAX/latest/actions/create-a-prompt', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "version": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes |  |
| `version` | object | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "2026-05-07T12:00:00.000Z",
      "created_by_user_id": "string",
      "description": "string",
      "id": "string",
      "name": "Ava Chen",
      "space_id": "string",
      "updated_at": "2026-05-07T12:00:00.000Z",
      "version": {
        "commit_hash": "string",
        "commit_message": "string",
        "created_at": "2026-05-07T12:00:00.000Z",
        "created_by_user_id": "string",
        "id": "string",
        "input_variable_format": "string",
        "invocation_params": {
          "tool_config": {
            "tool_choice": "string"
          }
        },
        "model": "string",
        "prompt_id": "string",
        "provider": "string",
        "tool_config": {
          "tool_choice": "string"
        }
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | date |  |
| `created_by_user_id` | string |  |
| `description` | string |  |
| `id` | string |  |
| `name` | string |  |
| `space_id` | string |  |
| `updated_at` | date |  |
| `version.commit_hash` | string |  |
| `version.commit_message` | string |  |
| `version.created_at` | date |  |
| `version.created_by_user_id` | string |  |
| `version.id` | string |  |
| `version.input_variable_format` | string |  |
| `version.invocation_params.tool_config.tool_choice` | string |  |
| `version.model` | string |  |
| `version.prompt_id` | string |  |
| `version.provider` | string |  |
| `version.tool_config.tool_choice` | string |  |

## Native endpoint

Through the native Arize AX API, this operation is `POST /v2/prompts` (base URL `https://api.arize.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-a-prompt.md) for the provider-specific parameters and requirements.

