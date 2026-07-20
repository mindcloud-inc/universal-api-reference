# CallRail: List Calls

Retrieves calls from CallRail.

```
GET https://connect.mindcloud.co/v1/universal/callRail/latest/actions/list-calls
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CallRail `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/callRail/latest/actions/list-calls?connectionId=$CONNECTION_ID&limit=25&offset=0&account_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "account_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/callRail/latest/actions/list-calls?${params}`, {
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
| `account_id` | string | yes | The CallRail account ID. |
| `company_id` | string | no | Optional company ID to limit calls to one company. |
| `tracker_id` | string | no | Optional tracker ID to limit calls to one tracking number. |
| `date_range` | string | no | Optional preset date range such as recent or today. |
| `start_date` | string | no | Optional ISO 8601 start date for a custom date range. |
| `end_date` | string | no | Optional ISO 8601 end date for a custom date range. |
| `search` | string | no | Optional search text for customer, number, note, or source fields. |
| `fields` | string | no | Optional comma-separated additional call fields to return. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "answered": true,
      "businessPhoneNumber": "string",
      "customerCity": "string",
      "customerCountry": "string",
      "customerName": "Ava Chen",
      "customerPhoneNumber": "string",
      "customerState": "string",
      "direction": "string",
      "duration": 1,
      "id": "string",
      "leadExplanation": "string",
      "leadScore": "string",
      "recording": "string",
      "recordingDuration": 1,
      "recordingPlayer": "string",
      "startTime": "string",
      "trackingPhoneNumber": "string",
      "voicemail": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `answered` | boolean |  |
| `businessPhoneNumber` | string |  |
| `customerCity` | string |  |
| `customerCountry` | string |  |
| `customerName` | string |  |
| `customerPhoneNumber` | string |  |
| `customerState` | string |  |
| `direction` | string |  |
| `duration` | number |  |
| `id` | string |  |
| `leadExplanation` | string |  |
| `leadScore` | string |  |
| `recording` | string |  |
| `recordingDuration` | number |  |
| `recordingPlayer` | string |  |
| `startTime` | string |  |
| `trackingPhoneNumber` | string |  |
| `voicemail` | boolean |  |

## Native endpoint

Through the native CallRail API, this operation is `GET /v3/a/:account_id/calls.json` (base URL `https://api.callrail.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-calls.md) for the provider-specific parameters and requirements.

