# HelpSpace: Delete Ticket

Deletes a ticket from HelpSpace.

```
DELETE https://connect.mindcloud.co/v1/universal/helpSpace/latest/actions/delete-ticket
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HelpSpace `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/helpSpace/latest/actions/delete-ticket?connectionId=$CONNECTION_ID&ticketId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "ticketId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/helpSpace/latest/actions/delete-ticket?${params}`, {
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
| `ticketId` | string | yes | HelpSpace ticket identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |

## Native endpoint

Through the native HelpSpace API, this operation is `DELETE /tickets/{id}` (base URL `https://api.helpspace.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-ticket.md) for the provider-specific parameters and requirements.

