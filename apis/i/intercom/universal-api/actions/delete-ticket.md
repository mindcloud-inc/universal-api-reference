# Intercom: Delete Ticket



```
DELETE https://connect.mindcloud.co/v1/universal/intercom/latest/actions/delete-ticket
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Intercom `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/intercom/latest/actions/delete-ticket?connectionId=$CONNECTION_ID&ticketId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "ticketId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/intercom/latest/actions/delete-ticket?${params}`, {
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
| `ticketId` | string | yes | Intercom ticket identifier |

## Response

```json
{
  "success": true,
  "data": [
    {
      "deleted": true,
      "id": "string",
      "object": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deleted` | boolean |  |
| `id` | string |  |
| `object` | string |  |

## Native endpoint

Through the native Intercom API, this operation is `DELETE /tickets/:ticket_id` (base URL `https://api.intercom.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-ticket.md) for the provider-specific parameters and requirements.

