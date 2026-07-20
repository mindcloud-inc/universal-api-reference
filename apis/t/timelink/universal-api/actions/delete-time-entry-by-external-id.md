# Timelink: Delete Time Entry by External ID

Deletes an existing time entry from Timelink by external ID.

```
DELETE https://connect.mindcloud.co/v1/universal/timelink/latest/actions/delete-time-entry-by-external-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Timelink `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/timelink/latest/actions/delete-time-entry-by-external-id?connectionId=$CONNECTION_ID&extId=stage3-time-entry-001" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "extId": "stage3-time-entry-001"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/timelink/latest/actions/delete-time-entry-by-external-id?${params}`, {
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
| `extId` | string | yes | The external reference ID for the time entry. Example: `stage3-time-entry-001`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |

## Native endpoint

Through the native Timelink API, this operation is `DELETE /timeEntries/ext/:extId` (base URL `https://api.timelink.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-time-entry-by-external-id.md) for the provider-specific parameters and requirements.

