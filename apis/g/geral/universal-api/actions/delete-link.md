# Geral: Delete Link

Deletes a link from Geral.

```
DELETE https://connect.mindcloud.co/v1/universal/geral/latest/actions/delete-link
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Geral `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/geral/latest/actions/delete-link?connectionId=$CONNECTION_ID&linkId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "linkId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/geral/latest/actions/delete-link?${params}`, {
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
| `linkId` | number | yes | The link ID to delete. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Geral API returns.

## Native endpoint

Through the native Geral API, this operation is `DELETE /links/:link_id` (base URL `https://ger.al/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-link.md) for the provider-specific parameters and requirements.

