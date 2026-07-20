# Billingo: List Document Reminders

Retrieves document reminders from Billingo by status.

```
GET https://connect.mindcloud.co/v1/universal/billingo/latest/actions/list-document-reminders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Billingo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/billingo/latest/actions/list-document-reminders?connectionId=$CONNECTION_ID&id=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "0"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/billingo/latest/actions/list-document-reminders?${params}`, {
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
| `id` | number | yes | Billingo document ID. Default: `0`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "sent_postal_mail": [
        {}
      ],
      "sent_reminders": [
        {}
      ],
      "upcoming_reminders": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `sent_postal_mail` | array<object> | Sent postal-mail reminder events. |
| `sent_reminders` | array<object> | Sent document reminder events. |
| `upcoming_reminders` | array<object> | Upcoming document reminder events. |

## Native endpoint

Through the native Billingo API, this operation is `GET /documents/:id/reminders` (base URL `https://api.billingo.hu/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-document-reminders.md) for the provider-specific parameters and requirements.

