# CATS: Delete Pipeline

Deletes an existing pipeline from CATS.

```
DELETE https://connect.mindcloud.co/v1/universal/cATS/latest/actions/delete-pipeline
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CATS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/cATS/latest/actions/delete-pipeline?connectionId=$CONNECTION_ID&id=319362285" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "319362285"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cATS/latest/actions/delete-pipeline?${params}`, {
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
| `id` | number | yes | The ID of the pipeline to delete. Example: `319362285`. |
| `createActivity` | boolean | no | Whether a corresponding activity should be created automatically. Example: `false`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native CATS API returns.

## Native endpoint

Through the native CATS API, this operation is `DELETE /pipelines/:id` (base URL `https://api.catsone.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-pipeline.md) for the provider-specific parameters and requirements.

