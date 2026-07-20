# Trackabi: Delete Time Entry

Deletes an existing time entry from Trackabi.

```
DELETE https://connect.mindcloud.co/v1/universal/trackabi/latest/actions/delete-time-entry
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Trackabi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/trackabi/latest/actions/delete-time-entry?connectionId=$CONNECTION_ID&timeEntryId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "timeEntryId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/trackabi/latest/actions/delete-time-entry?${params}`, {
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
| `timeEntryId` | number | yes | The unique ID of the time entry. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Trackabi API returns.

## Native endpoint

Through the native Trackabi API, this operation is `DELETE /api/v1/time-entry/:timeEntryId` (base URL `https://api.trackabi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-time-entry.md) for the provider-specific parameters and requirements.

