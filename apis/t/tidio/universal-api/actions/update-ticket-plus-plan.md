# Tidio: Update Ticket [Plus plan]

Updates a ticket in the Tidio workspace.

```
PUT https://connect.mindcloud.co/v1/universal/tidio/latest/actions/update-ticket-plus-plan
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tidio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/tidio/latest/actions/update-ticket-plus-plan" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "ticketId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/tidio/latest/actions/update-ticket-plus-plan', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "ticketId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `ticketId` | string | yes | The Tidio ticket ID. |
| `status` | string | no | Updated ticket status. |
| `priority` | string | no | Updated ticket priority. |
| `assigned.type` | string | no | Assignment target type: department or operator. |
| `assigned.id` | string | no | UUID of the assigned department or operator. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `value` | string | The raw response body. Tidio docs specify 204 Ticket has been updated correctly. |

## Native endpoint

Through the native Tidio API, this operation is `PATCH /tickets/{ticketId}` (base URL `https://api.tidio.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-ticket-plus-plan.md) for the provider-specific parameters and requirements.

