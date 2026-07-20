# Linkbreakers: List Workflow Steps for a Link

Retrieves workflow steps for a link in Linkbreakers.

```
GET https://connect.mindcloud.co/v1/universal/linkbreakers/latest/actions/list-workflow-steps-for-a-link
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Linkbreakers `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/linkbreakers/latest/actions/list-workflow-steps-for-a-link?connectionId=$CONNECTION_ID&limit=25&offset=0&linkId=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "linkId": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/linkbreakers/latest/actions/list-workflow-steps-for-a-link?${params}`, {
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
| `linkId` | string | yes | The ID of the link to list workflow steps for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "nextPageToken": "string",
      "workflowSteps": [
        {
          "canvasPosition": {},
          "childStepIds": [
            "string"
          ],
          "createdAt": "string",
          "eventAction": "string",
          "id": "string",
          "kind": "string",
          "linkId": "https://example.com",
          "nodeType": "string",
          "parentStepIds": [
            "string"
          ],
          "payload": {},
          "updatedAt": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `nextPageToken` | string |  |
| `workflowSteps` | array<object> | Workflow steps for the requested link. |
| `workflowSteps[].canvasPosition` | object |  |
| `workflowSteps[].childStepIds` | array<string> |  |
| `workflowSteps[].createdAt` | string |  |
| `workflowSteps[].eventAction` | string |  |
| `workflowSteps[].id` | string |  |
| `workflowSteps[].kind` | string |  |
| `workflowSteps[].linkId` | string |  |
| `workflowSteps[].nodeType` | string |  |
| `workflowSteps[].parentStepIds` | array<string> |  |
| `workflowSteps[].payload` | object |  |
| `workflowSteps[].updatedAt` | string |  |

## Native endpoint

Through the native Linkbreakers API, this operation is `GET /v1/links/:linkId/workflow-steps` (base URL `https://api.linkbreakers.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-workflow-steps-for-a-link.md) for the provider-specific parameters and requirements.

