# Productlane: Get Project

Retrieves a project from a Productlane portal.

```
GET https://connect.mindcloud.co/v1/universal/productlane/latest/actions/get-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Productlane `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/productlane/latest/actions/get-project?connectionId=$CONNECTION_ID&workspaceId=ba9bf7e6-fc19-40d3-9174-275a63e5fa74&projectId=project-id" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workspaceId": "ba9bf7e6-fc19-40d3-9174-275a63e5fa74",
  "projectId": "project-id"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/productlane/latest/actions/get-project?${params}`, {
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
| `workspaceId` | string | yes | Workspace ID to read the public project from. Example: `ba9bf7e6-fc19-40d3-9174-275a63e5fa74`. |
| `projectId` | string | yes | Project ID. Example: `project-id`. |
| `language` | string | no | Optional language override. Example: `en`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Productlane API returns.

## Native endpoint

Through the native Productlane API, this operation is `GET /projects/{workspaceId}/{projectId}` (base URL `https://productlane.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project.md) for the provider-specific parameters and requirements.

