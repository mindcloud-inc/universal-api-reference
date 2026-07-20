# Filestage: Remove Project by ID

Deletes a project from Filestage by ID.

```
DELETE https://connect.mindcloud.co/v1/universal/filestage/latest/actions/remove-project-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Filestage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/filestage/latest/actions/remove-project-by-id?connectionId=$CONNECTION_ID&projectId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/filestage/latest/actions/remove-project-by-id?${params}`, {
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
| `projectId` | string | yes | Project Id |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Filestage API returns.

## Native endpoint

Through the native Filestage API, this operation is `DELETE /projects/{projectId}` (base URL `https://api.filestage.io/ext/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-project-by-id.md) for the provider-specific parameters and requirements.

