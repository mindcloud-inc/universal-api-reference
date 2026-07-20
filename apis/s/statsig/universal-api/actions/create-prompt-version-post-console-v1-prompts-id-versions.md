# Statsig: Create Prompt Version

Creates a prompt version in Statsig.

```
POST https://connect.mindcloud.co/v1/universal/statsig/latest/actions/create-prompt-version-post-console-v1-prompts-id-versions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Statsig `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/statsig/latest/actions/create-prompt-version-post-console-v1-prompts-id-versions" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/statsig/latest/actions/create-prompt-version-post-console-v1-prompts-id-versions', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | id |
| `prompts` | list | no | Request body field. |
| `temperature` | number | no | Request body field. |
| `model` | string | no | Request body field. |
| `name` | string | yes | Request body field. |
| `provider` | string | no | Request body field. |
| `workflowBody` | object | no | Request body field. |
| `workflowHeaders` | list | no | Request body field. |
| `authWorkflowHeaders` | list | no | Request body field. |
| `evalModel` | string | no | Request body field. |
| `topP` | number | no | Request body field. |
| `frequencyPenalty` | number | no | Request body field. |
| `presencePenalty` | number | no | Request body field. |
| `maxTokens` | number | no | Request body field. |
| `description` | string | no | Request body field. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Statsig response data payload. |
| `message` | string | Statsig response message. |

## Native endpoint

Through the native Statsig API, this operation is `POST /console/v1/prompts/{id}/versions` (base URL `https://statsigapi.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-prompt-version-post-console-v1-prompts-id-versions.md) for the provider-specific parameters and requirements.

