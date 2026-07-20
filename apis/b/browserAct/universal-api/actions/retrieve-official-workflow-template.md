# BrowserAct: Retrieve Official Workflow Template

Retrieves an official workflow template from BrowserAct.

```
GET https://connect.mindcloud.co/v1/universal/browserAct/latest/actions/retrieve-official-workflow-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BrowserAct `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/browserAct/latest/actions/retrieve-official-workflow-template?connectionId=$CONNECTION_ID&workflowTemplateId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workflowTemplateId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/browserAct/latest/actions/retrieve-official-workflow-template?${params}`, {
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
| `workflowTemplateId` | string | yes | Official BrowserAct workflow template ID to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createAt": "string",
      "description": "string",
      "detailUrl": "https://example.com",
      "id": "string",
      "name": "Ava Chen",
      "publishAt": "string",
      "recommendDesc": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createAt` | string | Template creation timestamp. |
| `description` | string | Template description. |
| `detailUrl` | string | Public template detail URL. |
| `id` | string | Workflow template ID. |
| `name` | string | Template name. |
| `publishAt` | string | Template publish timestamp. |
| `recommendDesc` | string | Recommended use case description. |

## Native endpoint

Through the native BrowserAct API, this operation is `GET /get-official-workflow-template` (base URL `https://api.browseract.com/v2/workflow`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-official-workflow-template.md) for the provider-specific parameters and requirements.

