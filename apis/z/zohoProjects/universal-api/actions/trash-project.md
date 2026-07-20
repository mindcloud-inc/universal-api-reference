# Zoho Projects: Trash Project

Trashes an existing project in Zoho Projects.

```
DELETE https://connect.mindcloud.co/v1/universal/zohoProjects/latest/actions/trash-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Projects `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/zohoProjects/latest/actions/trash-project?connectionId=$CONNECTION_ID&portalId=string&projectId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "portalId": "string",
  "projectId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoProjects/latest/actions/trash-project?${params}`, {
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
| `portalId` | string | yes | Portal identifier from Zoho Projects. |
| `projectId` | string | yes | Project identifier from Zoho Projects. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Zoho Projects API returns.

## Native endpoint

Through the native Zoho Projects API, this operation is `POST /portal/[:PORTALID]/projects/[:PROJECTID]/trash` (base URL `https://projectsapi.zoho.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/trash-project.md) for the provider-specific parameters and requirements.

