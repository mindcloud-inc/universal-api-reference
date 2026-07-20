# Skyvern: List Workflows

Retrieves workflows and their latest versions from Skyvern.

```
GET https://connect.mindcloud.co/v1/universal/skyvern/latest/actions/list-workflows
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Skyvern `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/skyvern/latest/actions/list-workflows?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/skyvern/latest/actions/list-workflows?${params}`, {
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
| `folderId` | string | no | Filter workflows by folder ID. |
| `onlySavedTasks` | boolean | no |  |
| `onlyTemplates` | boolean | no |  |
| `onlyWorkflows` | boolean | no |  |
| `searchKey` | string | no | Case-insensitive substring search across workflow title, folder name, and parameter metadata. |
| `status[]` | array<string> | no |  |
| `template` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "adaptiveCaching": true,
      "aiFallback": true,
      "cacheKey": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "deletedAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "extraHttpHeaders": {},
      "folderId": "string",
      "generateScriptOnTerminal": true,
      "importError": "string",
      "isSavedTask": true,
      "isTemplate": true,
      "maxScreenshotScrolls": 1,
      "model": {},
      "modifiedAt": "2026-05-07T12:00:00.000Z",
      "organizationId": "string",
      "persistBrowserSession": true,
      "proxyLocation": {},
      "runSequentially": true,
      "runWith": "string",
      "sequentialKey": "string",
      "status": "string",
      "title": "string",
      "totpIdentifier": "string",
      "totpVerificationUrl": "https://example.com",
      "version": 1,
      "webhookCallbackUrl": "https://example.com",
      "workflowDefinition": {},
      "workflowId": "string",
      "workflowPermanentId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `adaptiveCaching` | boolean | Whether adaptive caching is enabled |
| `aiFallback` | boolean | Whether the workflow can fall back to AI |
| `cacheKey` | string | Workflow cache key |
| `createdAt` | date | Workflow creation timestamp |
| `deletedAt` | date | Workflow deletion timestamp |
| `description` | string | Workflow description |
| `extraHttpHeaders` | object | Additional HTTP headers used by the workflow |
| `folderId` | string | Folder ID |
| `generateScriptOnTerminal` | boolean | Whether to generate script output on the terminal |
| `importError` | string | Import error message, when present |
| `isSavedTask` | boolean | Whether this workflow is saved as a task |
| `isTemplate` | boolean | Whether this workflow is a template |
| `maxScreenshotScrolls` | number | Maximum number of screenshot scrolls |
| `model` | object | Model configuration |
| `modifiedAt` | date | Workflow last modification timestamp |
| `organizationId` | string | Organization ID |
| `persistBrowserSession` | boolean | Whether the browser session is persisted |
| `proxyLocation` | object | Proxy location configuration |
| `runSequentially` | boolean | Whether workflow runs are forced to be sequential |
| `runWith` | string | Execution mode used for this workflow |
| `sequentialKey` | string | Sequential execution key |
| `status` | string | Workflow status |
| `title` | string | Workflow title |
| `totpIdentifier` | string | TOTP identifier |
| `totpVerificationUrl` | string | TOTP verification URL |
| `version` | number | Workflow version |
| `webhookCallbackUrl` | string | Webhook callback URL |
| `workflowDefinition` | object | Workflow definition payload |
| `workflowId` | string | Workflow ID |
| `workflowPermanentId` | string | Permanent workflow identifier |

## Native endpoint

Through the native Skyvern API, this operation is `GET /v1/workflows` (base URL `https://api.skyvern.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-workflows.md) for the provider-specific parameters and requirements.

