# Arize AX: Get a Prompt Version

Retrieves a prompt version from Arize AX.

```
GET https://connect.mindcloud.co/v1/universal/arizeAX/latest/actions/get-a-prompt-version
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Arize AX `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/arizeAX/latest/actions/get-a-prompt-version?connectionId=$CONNECTION_ID&versionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "versionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/arizeAX/latest/actions/get-a-prompt-version?${params}`, {
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
| `versionId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "commitHash": "string",
      "commitMessage": "string",
      "createdAt": "string",
      "createdByUserId": "string",
      "id": "string",
      "inputVariableFormat": "string",
      "invocationParams": {},
      "labels": [
        "string"
      ],
      "messages": [
        {}
      ],
      "model": "string",
      "promptId": "string",
      "provider": "string",
      "providerParams": {},
      "toolConfig": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `commitHash` | string | Version commit hash |
| `commitMessage` | string | Version commit message |
| `createdAt` | string | Creation timestamp |
| `createdByUserId` | string | Creator user ID |
| `id` | string | Prompt version ID |
| `inputVariableFormat` | string | Prompt input variable format |
| `invocationParams` | object | Invocation parameters |
| `labels` | array<string> | Version labels |
| `messages` | array<object> | Prompt messages |
| `model` | string | Model name |
| `promptId` | string | Parent prompt ID |
| `provider` | string | Provider name |
| `providerParams` | object | Provider parameters |
| `toolConfig` | object | Tool configuration |

## Native endpoint

Through the native Arize AX API, this operation is `GET /v2/prompt-versions/:version_id` (base URL `https://api.arize.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-a-prompt-version.md) for the provider-specific parameters and requirements.

