# Ticketbud: Get Event Totals

Retrieves event totals from Ticketbud.

```
GET https://connect.mindcloud.co/v1/universal/ticketbud/latest/actions/get-event-totals
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ticketbud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ticketbud/latest/actions/get-event-totals?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ticketbud/latest/actions/get-event-totals?${params}`, {
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
| `id` | string | yes | The Ticketbud event ID to retrieve totals for. |

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
| `event` | object | The totals payload for the requested Ticketbud event. |

## Native endpoint

Through the native Ticketbud API, this operation is `GET /events/:id/totals.json` (base URL `https://api.ticketbud.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-event-totals.md) for the provider-specific parameters and requirements.

