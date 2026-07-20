# UniOne: Delete Project

Deletes an existing project from UniOne.

```
DELETE https://connect.mindcloud.co/v1/universal/uniOne/latest/actions/delete-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a UniOne `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/uniOne/latest/actions/delete-project?connectionId=$CONNECTION_ID&projectId=6123462132634" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "6123462132634"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/uniOne/latest/actions/delete-project?${params}`, {
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
| `projectId` | string | yes | Unique project identifier. Example: `6123462132634`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native UniOne API returns.

## Native endpoint

Through the native UniOne API, this operation is `POST project/delete.json` (base URL `https://api.unione.io/en/transactional/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-project.md) for the provider-specific parameters and requirements.

