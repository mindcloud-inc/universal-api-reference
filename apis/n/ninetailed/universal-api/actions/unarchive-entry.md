# Ninetailed: Unarchive Entry



```
PUT https://connect.mindcloud.co/v1/universal/ninetailed/latest/actions/unarchive-entry
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ninetailed `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/ninetailed/latest/actions/unarchive-entry" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "spaceId": "string",
  "environmentId": "master",
  "entryId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ninetailed/latest/actions/unarchive-entry', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "spaceId": "string",
    "environmentId": "master",
    "entryId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `spaceId` | string | yes | Contentful space ID. |
| `environmentId` | string | yes | Contentful environment ID, such as master. Default: `master`. |
| `entryId` | string | yes | Entry ID to unarchive. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Ninetailed API returns.

## Native endpoint

Through the native Ninetailed API, this operation is `DELETE /spaces/:spaceId/environments/:environmentId/entries/:entryId/archived` (base URL `https://api.contentful.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/unarchive-entry.md) for the provider-specific parameters and requirements.

