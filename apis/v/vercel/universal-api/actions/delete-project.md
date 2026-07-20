# Vercel: Delete Project

Deletes an existing project from Vercel.

```
DELETE https://connect.mindcloud.co/v1/universal/vercel/latest/actions/delete-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vercel `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/vercel/latest/actions/delete-project?connectionId=$CONNECTION_ID&idOrName=prj_1234567890" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "idOrName": "prj_1234567890"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vercel/latest/actions/delete-project?${params}`, {
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
| `idOrName` | string | yes | The unique project identifier or the project name Example: `prj_1234567890`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Vercel API returns.

## Native endpoint

Through the native Vercel API, this operation is `DELETE /v9/projects/:idOrName` (base URL `https://api.vercel.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-project.md) for the provider-specific parameters and requirements.

