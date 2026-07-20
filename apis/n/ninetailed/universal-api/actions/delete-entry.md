# Ninetailed: Delete Entry



```
DELETE https://connect.mindcloud.co/v1/universal/ninetailed/latest/actions/delete-entry
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ninetailed `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/ninetailed/latest/actions/delete-entry?connectionId=$CONNECTION_ID&spaceId=string&environmentId=master&entryId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "spaceId": "string",
  "environmentId": "master",
  "entryId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ninetailed/latest/actions/delete-entry?${params}`, {
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
| `spaceId` | string | yes | Contentful space ID. |
| `environmentId` | string | yes | Contentful environment ID, such as master. Default: `master`. |
| `entryId` | string | yes | Entry ID to delete. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Ninetailed API returns.

## Native endpoint

Through the native Ninetailed API, this operation is `DELETE /spaces/:spaceId/environments/:environmentId/entries/:entryId` (base URL `https://api.contentful.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-entry.md) for the provider-specific parameters and requirements.

