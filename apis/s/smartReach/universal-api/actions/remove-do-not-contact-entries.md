# SmartReach: Remove Do Not Contact Entries

Deletes do not contact entries from SmartReach.

```
DELETE https://connect.mindcloud.co/v1/universal/smartReach/latest/actions/remove-do-not-contact-entries
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SmartReach `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/smartReach/latest/actions/remove-do-not-contact-entries?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smartReach/latest/actions/remove-do-not-contact-entries?${params}`, {
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
| `dncIds[]` | array<string> | no | Ids of do_not_contact to be deleted |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native SmartReach API returns.

## Native endpoint

Through the native SmartReach API, this operation is `DELETE /do_not_contact` (base URL `https://api.smartreach.io/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-do-not-contact-entries.md) for the provider-specific parameters and requirements.

