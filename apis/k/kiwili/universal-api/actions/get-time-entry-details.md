# Kiwili: Get Time Entry Details

Retrieves details for a time entry in Kiwili.

```
GET https://connect.mindcloud.co/v1/universal/kiwili/latest/actions/get-time-entry-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kiwili `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kiwili/latest/actions/get-time-entry-details?connectionId=$CONNECTION_ID&time_entry_id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "time_entry_id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kiwili/latest/actions/get-time-entry-details?${params}`, {
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
| `time_entry_id` | number | yes | The Kiwili time entry ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Description": "string",
      "EntryDate": "string",
      "Hours": 1,
      "Id": 1,
      "ProjectId": 1,
      "TaskId": 1,
      "UserId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Description` | string |  |
| `EntryDate` | string |  |
| `Hours` | number |  |
| `Id` | number |  |
| `ProjectId` | number |  |
| `TaskId` | number |  |
| `UserId` | number |  |

## Native endpoint

Through the native Kiwili API, this operation is `GET /timeentry/:time_entry_id` (base URL `https://mindcloud.kiwili.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-time-entry-details.md) for the provider-specific parameters and requirements.

