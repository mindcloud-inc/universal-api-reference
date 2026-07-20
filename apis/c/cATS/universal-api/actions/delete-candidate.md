# CATS: Delete Candidate

Deletes an existing candidate from CATS.

```
DELETE https://connect.mindcloud.co/v1/universal/cATS/latest/actions/delete-candidate
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CATS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/cATS/latest/actions/delete-candidate?connectionId=$CONNECTION_ID&id=411876229" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "411876229"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cATS/latest/actions/delete-candidate?${params}`, {
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
| `id` | number | yes | The ID of the candidate to delete. Example: `411876229`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native CATS API returns.

## Native endpoint

Through the native CATS API, this operation is `DELETE /candidates/:id` (base URL `https://api.catsone.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-candidate.md) for the provider-specific parameters and requirements.

