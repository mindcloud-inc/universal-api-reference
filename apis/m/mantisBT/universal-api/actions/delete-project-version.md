# MantisBT: Delete Project Version

Deletes a project version from MantisBT.

```
DELETE https://connect.mindcloud.co/v1/universal/mantisBT/latest/actions/delete-project-version
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MantisBT `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/mantisBT/latest/actions/delete-project-version?connectionId=$CONNECTION_ID&projectId=1&versionId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "1",
  "versionId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mantisBT/latest/actions/delete-project-version?${params}`, {
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
| `projectId` | number | yes | ID of the project that owns the version |
| `versionId` | number | yes | ID of the version to delete |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native MantisBT API returns.

## Native endpoint

Through the native MantisBT API, this operation is `DELETE /projects/{project_id}/versions/{version_id}` (base URL `{{credentials.baseUrl}}/api/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-project-version.md) for the provider-specific parameters and requirements.

