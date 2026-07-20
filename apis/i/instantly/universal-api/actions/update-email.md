# Instantly: Update Email

Updates an existing email in Instantly.

```
PUT https://connect.mindcloud.co/v1/universal/instantly/latest/actions/update-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Instantly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/instantly/latest/actions/update-email" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/instantly/latest/actions/update-email', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Email UUID. |
| `isUnread` | number | no | Unread flag. |
| `reminderTs` | date | no | Reminder timestamp. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "is_unread": 1,
      "reminder_ts": "2026-05-07T12:00:00.000Z",
      "subject": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Email ID. |
| `is_unread` | number | Unread flag. |
| `reminder_ts` | date | Reminder timestamp. |
| `subject` | string | Subject. |

## Native endpoint

Through the native Instantly API, this operation is `PATCH /api/v2/emails/:id` (base URL `https://api.instantly.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-email.md) for the provider-specific parameters and requirements.

