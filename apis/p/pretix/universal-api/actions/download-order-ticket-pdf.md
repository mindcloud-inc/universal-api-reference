# pretix: Download Order Ticket PDF

Retrieves an order ticket PDF from pretix.

```
GET https://connect.mindcloud.co/v1/universal/pretix/latest/actions/download-order-ticket-pdf
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a pretix `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pretix/latest/actions/download-order-ticket-pdf?connectionId=$CONNECTION_ID&organizer=string&event=string&code=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organizer": "string",
  "event": "string",
  "code": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pretix/latest/actions/download-order-ticket-pdf?${params}`, {
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
| `organizer` | string | yes | pretix organizer slug. |
| `event` | string | yes | pretix event slug. |
| `code` | string | yes | pretix order code. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native pretix API returns.

## Native endpoint

Through the native pretix API, this operation is `GET /organizers/:organizer/events/:event/orders/:code/download/pdf/` (base URL `https://pretix.eu/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/download-order-ticket-pdf.md) for the provider-specific parameters and requirements.

