# Zoho Projects: Delete Issue

Deletes an existing issue from Zoho Projects.

```
DELETE https://connect.mindcloud.co/v1/universal/zohoProjects/latest/actions/delete-issue
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Projects `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/zohoProjects/latest/actions/delete-issue?connectionId=$CONNECTION_ID&portalId=string&projectId=string&issueId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "portalId": "string",
  "projectId": "string",
  "issueId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoProjects/latest/actions/delete-issue?${params}`, {
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
| `portalId` | string | yes | Zoho Projects portal ID. |
| `projectId` | string | yes | Zoho Projects project ID. |
| `issueId` | string | yes | Zoho Projects issue ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Zoho Projects API returns.

## Native endpoint

Through the native Zoho Projects API, this operation is `DELETE /portal/[:PORTALID]/projects/[:PROJECTID]/issues/[:ISSUEID]` (base URL `https://projectsapi.zoho.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-issue.md) for the provider-specific parameters and requirements.

