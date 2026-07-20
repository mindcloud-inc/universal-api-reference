# MantisBT: Update Project Version

Updates an existing project version in MantisBT.

```
PUT https://connect.mindcloud.co/v1/universal/mantisBT/latest/actions/update-project-version
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MantisBT `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/mantisBT/latest/actions/update-project-version" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "obsolete": true,
  "projectId": 1,
  "versionId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mantisBT/latest/actions/update-project-version', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "obsolete": true,
    "projectId": 1,
    "versionId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `obsolete` | boolean | yes | Whether the version should be marked obsolete |
| `projectId` | number | yes | ID of the project that owns the version |
| `versionId` | number | yes | ID of the version to update |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native MantisBT API returns.

## Native endpoint

Through the native MantisBT API, this operation is `PATCH /projects/{project_id}/versions/{version_id}` (base URL `{{credentials.baseUrl}}/api/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-project-version.md) for the provider-specific parameters and requirements.

