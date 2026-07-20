# Ticketbud: Get Event Sales Summary

Retrieves an event sales summary from Ticketbud.

```
GET https://connect.mindcloud.co/v1/universal/ticketbud/latest/actions/get-event-sales-summary
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ticketbud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ticketbud/latest/actions/get-event-sales-summary?connectionId=$CONNECTION_ID&eventId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "eventId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ticketbud/latest/actions/get-event-sales-summary?${params}`, {
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
| `eventId` | string | yes | The Ticketbud event ID to retrieve sales summary for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "event": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `event` | object | The sales summary payload for the requested Ticketbud event. |

## Native endpoint

Through the native Ticketbud API, this operation is `GET /events/:eventId/ticket_sales` (base URL `https://api.ticketbud.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-event-sales-summary.md) for the provider-specific parameters and requirements.

