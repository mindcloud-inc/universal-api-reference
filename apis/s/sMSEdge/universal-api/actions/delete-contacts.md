# SMSEdge: Delete Contacts

Deletes contacts from a SMSEdge list.

```
DELETE https://connect.mindcloud.co/v1/universal/sMSEdge/latest/actions/delete-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SMSEdge `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/sMSEdge/latest/actions/delete-contacts?connectionId=$CONNECTION_ID&ids=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "ids": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sMSEdge/latest/actions/delete-contacts?${params}`, {
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
| `ids` | string | yes | Comma-separated IDs of numbers to be deleted |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native SMSEdge API returns.

## Native endpoint

Through the native SMSEdge API, this operation is `DELETE /numbers/delete/` (base URL `https://api.smsedge.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-contacts.md) for the provider-specific parameters and requirements.

