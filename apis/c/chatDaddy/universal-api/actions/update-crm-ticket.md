# ChatDaddy: Update CRM Ticket

Updates an existing CRM ticket in ChatDaddy.

```
PUT https://connect.mindcloud.co/v1/universal/chatDaddy/latest/actions/update-crm-ticket
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ChatDaddy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/chatDaddy/latest/actions/update-crm-ticket" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "sample-ticket-id"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chatDaddy/latest/actions/update-crm-ticket', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "sample-ticket-id"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | CRM ticket identifier to update. Default: `sample-ticket-id`. |
| `title` | string | no | Updated CRM ticket title. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true,
      "updated": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean | Whether the CRM ticket update completed successfully. |
| `updated` | number | How many CRM tickets were updated. |

## Native endpoint

Through the native ChatDaddy API, this operation is `PATCH /crm/tickets/{id}` (base URL `https://api.chatdaddy.tech/im`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-crm-ticket.md) for the provider-specific parameters and requirements.

