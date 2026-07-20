# Abyssale: Duplicate Workspace Template

Duplicates a workspace template into an Abyssale project.

```
POST https://connect.mindcloud.co/v1/universal/abyssale/latest/actions/duplicate-workspace-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Abyssale `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/abyssale/latest/actions/duplicate-workspace-template" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "companyTemplateId": "0c967bd0-4137-4690-ad70-249aa021c68b",
  "project_id": "d59adee9-4867-11f0-96f2-0a00d9eb8f78"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/abyssale/latest/actions/duplicate-workspace-template', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "companyTemplateId": "0c967bd0-4137-4690-ad70-249aa021c68b",
    "project_id": "d59adee9-4867-11f0-96f2-0a00d9eb8f78"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `companyTemplateId` | string | yes | Workspace template UUID to duplicate Example: `0c967bd0-4137-4690-ad70-249aa021c68b`. |
| `project_id` | string | yes | Target project ID where the template will be duplicated Example: `d59adee9-4867-11f0-96f2-0a00d9eb8f78`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Abyssale API returns.

## Native endpoint

Through the native Abyssale API, this operation is `POST /workspace-templates/:companyTemplateId/use` (base URL `https://api.abyssale.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/duplicate-workspace-template.md) for the provider-specific parameters and requirements.

