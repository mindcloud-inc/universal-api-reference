# Scanova: Delete Lead List



```
DELETE https://connect.mindcloud.co/v1/universal/scanova/latest/actions/delete-lead-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Scanova `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/scanova/latest/actions/delete-lead-list?connectionId=$CONNECTION_ID&leadListId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "leadListId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scanova/latest/actions/delete-lead-list?${params}`, {
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
| `leadListId` | string | yes | Lead list ID (lead_id) |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Scanova API returns.

## Native endpoint

Through the native Scanova API, this operation is `DELETE /lead/{lead_list_id}/` (base URL `https://management.scanova.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-lead-list.md) for the provider-specific parameters and requirements.

