# Beebole: Reject Time Entry

Rejects a time entry in Beebole.

```
PUT https://connect.mindcloud.co/v1/universal/beebole/latest/actions/reject-time-entry
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Beebole `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/beebole/latest/actions/reject-time-entry" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "memo": "Rejected from MindCloud test"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/beebole/latest/actions/reject-time-entry', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "memo": "Rejected from MindCloud test"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `person.id` | number | no | Optional person identifier when rejecting a date range. Example: `2`. |
| `from` | string | no | Optional range start date in YYYY-MM-DD format. Example: `2026-03-01`. |
| `to` | string | no | Optional range end date in YYYY-MM-DD format. Example: `2026-03-31`. |
| `id` | number | no | Optional time entry identifier when rejecting one entry. |
| `date` | string | no | Optional time entry date in YYYY-MM-DD format when rejecting one entry. Example: `2026-03-23`. |
| `memo` | string | yes | The rejection reason sent to the employee via email. Example: `Rejected from MindCloud test`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Beebole API returns.

## Native endpoint

Through the native Beebole API, this operation is `POST` (base URL `https://beebole-apps.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/reject-time-entry.md) for the provider-specific parameters and requirements.

