# Timing: Delete Time Entry

Deletes an existing time entry from Timing.

```
DELETE https://connect.mindcloud.co/v1/universal/timing/latest/actions/delete-time-entry
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Timing `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/timing/latest/actions/delete-time-entry?connectionId=$CONNECTION_ID&timeEntryId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "timeEntryId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/timing/latest/actions/delete-time-entry?${params}`, {
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
| `timeEntryId` | string | yes | The Timing time entry ID to delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "response": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response` | string |  |

## Native endpoint

Through the native Timing API, this operation is `DELETE /time-entries/:time_entry_id` (base URL `https://web.timingapp.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-time-entry.md) for the provider-specific parameters and requirements.

