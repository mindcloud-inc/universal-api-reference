# ServiceTitan: Update Journal Entry Sync Status

Updates the sync status of a journal entry, for example marking it Synced after exporting it to an accounting system.

```
PUT https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/update-journal-entry-sync-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ServiceTitan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/update-journal-entry-sync-status" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "550e8400-e29b-41d4-a716-446655440000",
  "syncStatus": "Error"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/update-journal-entry-sync-status', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "550e8400-e29b-41d4-a716-446655440000",
    "syncStatus": "Error"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Example: `550e8400-e29b-41d4-a716-446655440000`. |
| `syncStatus` | list<string> | yes | One of: `Error`, `Excluded`, `InProgress`, `NotSynced`, `OutOfSync`, `Synced`. |
| `versionId` | number | no | The journal entry version that was synced. Required when Sync Status is Synced; ignored otherwise. |
| `message` | string | no | Message about the new sync state, such as the external reference or an error. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customFields` | object | no | Custom fields to create or update, as name/value pairs. Maximum 5 per journal entry. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ServiceTitan API returns.

## Native endpoint

Through the native ServiceTitan API, this operation is `PATCH accounting/v2/tenant/{{credentials.tenant}}/journal-entries/:id/sync` (base URL `https://{{credentials.baseUrl}}/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-journal-entry-sync-status.md) for the provider-specific parameters and requirements.

