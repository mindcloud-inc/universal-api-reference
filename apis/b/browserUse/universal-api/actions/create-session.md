# Browser Use: Create Session

Creates a session or dispatches a task in Browser Use.

```
POST https://connect.mindcloud.co/v1/universal/browserUse/latest/actions/create-session
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Browser Use `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/browserUse/latest/actions/create-session" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/browserUse/latest/actions/create-session', {
  method: 'POST',
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
| `model` | string | no | Model to use, such as claude-sonnet-4.6, gemini-3-flash, or claude-opus-4.6. |
| `profileId` | string | no | Browser profile ID to load into the session. |
| `proxyCountryCode` | string | no | Proxy country code such as us, de, or jp. Set null to disable proxy. |
| `sessionId` | string | no | Existing idle session ID to dispatch the task to. |
| `task` | string | no | Natural-language instruction for the agent to execute. |
| `workspaceId` | string | no | Workspace ID to attach to the session. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `agentmail` | boolean | no | Whether to provision a temporary AgentMail inbox. Default: `true`. |
| `cacheScript` | boolean | no | Controls deterministic script caching. |
| `enableRecording` | boolean | no | Whether to record the browser session. Default: `false`. |
| `enableScheduledTasks` | boolean | no | Whether the agent may create scheduled tasks. Default: `false`. |
| `keepAlive` | boolean | no | Keep the session idle after the task completes so follow-up tasks can reuse it. Default: `false`. |
| `maxCostUsd` | number | no | Maximum allowed cost in USD for this session. |
| `outputSchema` | object | no | JSON Schema object for structured task output. |
| `skills` | boolean | no | Whether to enable built-in Browser Use skills. Default: `true`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "isTaskSuccessful": true,
      "lastStepSummary": "string",
      "liveUrl": "https://example.com",
      "model": "string",
      "output": {},
      "profileId": "string",
      "recordingUrls": [
        "https://example.com"
      ],
      "status": "string",
      "stepCount": 1,
      "title": "string",
      "totalCostUsd": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "workspaceId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `id` | string |  |
| `isTaskSuccessful` | boolean |  |
| `lastStepSummary` | string |  |
| `liveUrl` | string |  |
| `model` | string |  |
| `output` | object |  |
| `profileId` | string |  |
| `recordingUrls` | array<string> |  |
| `status` | string |  |
| `stepCount` | number |  |
| `title` | string |  |
| `totalCostUsd` | string |  |
| `updatedAt` | date |  |
| `workspaceId` | string |  |

## Native endpoint

Through the native Browser Use API, this operation is `POST /sessions` (base URL `https://api.browser-use.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-session.md) for the provider-specific parameters and requirements.

