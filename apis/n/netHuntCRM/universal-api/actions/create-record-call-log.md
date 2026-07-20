# NetHunt CRM: Create Record Call Log

Creates a record call log in NetHunt CRM.

```
POST https://connect.mindcloud.co/v1/universal/netHuntCRM/latest/actions/create-record-call-log
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NetHunt CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/netHuntCRM/latest/actions/create-record-call-log" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "recordId": "string",
  "text": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/netHuntCRM/latest/actions/create-record-call-log', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "recordId": "string",
    "text": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `duration` | number | no | Call log duration in minutes. |
| `recordId` | string | yes | Record ID to create the call log for. |
| `text` | string | yes | Call log text. |
| `time` | date | no | ISO-formatted UTC time when the call started. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "callLogId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `callLogId` | string |  |
| `createdAt` | date |  |

## Native endpoint

Through the native NetHunt CRM API, this operation is `POST /actions/create-call-log/:recordId` (base URL `https://nethunt.com/api/v1/zapier`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-record-call-log.md) for the provider-specific parameters and requirements.

