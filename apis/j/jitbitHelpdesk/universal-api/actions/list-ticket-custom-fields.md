# Jitbit Helpdesk: List Ticket Custom Fields



```
GET https://connect.mindcloud.co/v1/universal/jitbitHelpdesk/latest/actions/list-ticket-custom-fields
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Jitbit Helpdesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jitbitHelpdesk/latest/actions/list-ticket-custom-fields?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/jitbitHelpdesk/latest/actions/list-ticket-custom-fields?${params}`, {
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
| `id` | number | yes | Jitbit ticket ID to list custom fields for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "fieldId": 1,
      "id": 1,
      "label": "string",
      "name": "Ava Chen",
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `fieldId` | number | Ticket custom field ID when present. |
| `id` | number | Field identifier when present. |
| `label` | string | Field label. |
| `name` | string | Field name. |
| `value` | string | Current custom field value. |

## Native endpoint

Through the native Jitbit Helpdesk API, this operation is `GET /TicketCustomFields` (base URL `{{credentials.helpdeskBaseUrl}}/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-ticket-custom-fields.md) for the provider-specific parameters and requirements.

