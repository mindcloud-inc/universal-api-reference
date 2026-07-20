# DataMerge: Delete List

Deletes an existing list from DataMerge.

```
DELETE https://connect.mindcloud.co/v1/universal/dataMerge/latest/actions/delete-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DataMerge `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/dataMerge/latest/actions/delete-list?connectionId=$CONNECTION_ID&objectType=string&list=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "objectType": "string",
  "list": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dataMerge/latest/actions/delete-list?${params}`, {
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
| `objectType` | string | yes |  |
| `list` | string | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native DataMerge API returns.

## Native endpoint

Through the native DataMerge API, this operation is `DELETE /v1/lists/:object_type/:list` (base URL `https://api.datamerge.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-list.md) for the provider-specific parameters and requirements.

