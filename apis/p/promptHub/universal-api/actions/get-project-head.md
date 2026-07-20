# PromptHub: Get Project Head

Retrieves a PromptHub project's head revision.

```
GET https://connect.mindcloud.co/v1/universal/promptHub/latest/actions/get-project-head
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PromptHub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/promptHub/latest/actions/get-project-head?connectionId=$CONNECTION_ID&projectId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/promptHub/latest/actions/get-project-head?${params}`, {
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
| `projectId` | string | yes | The PromptHub project ID. |
| `branch` | string | no | Use the head revision from a specific branch. |
| `fallback` | boolean | no | When true, unspecified variables fall back to PromptHub defaults. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native PromptHub API returns.

## Native endpoint

Through the native PromptHub API, this operation is `GET /projects/:projectId/head` (base URL `https://app.prompthub.us/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project-head.md) for the provider-specific parameters and requirements.

