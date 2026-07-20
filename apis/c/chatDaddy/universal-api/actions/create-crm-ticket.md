# ChatDaddy: Create CRM Ticket

Creates a new CRM ticket in ChatDaddy.

```
POST https://connect.mindcloud.co/v1/universal/chatDaddy/latest/actions/create-crm-ticket
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ChatDaddy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/chatDaddy/latest/actions/create-crm-ticket" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "boardId": "sample-board-id",
  "contactId": "sample-contact-id",
  "title": "Test CRM Ticket"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chatDaddy/latest/actions/create-crm-ticket', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "boardId": "sample-board-id",
    "contactId": "sample-contact-id",
    "title": "Test CRM Ticket"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `boardId` | string | yes | CRM board identifier for the ticket. Default: `sample-board-id`. |
| `contactId` | string | yes | Contact identifier to associate with the ticket. Default: `sample-contact-id`. |
| `stageId` | string | no | Optional CRM stage identifier for the ticket. |
| `title` | string | yes | CRM ticket title. Default: `Test CRM Ticket`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "boardId": "string",
      "contactId": "string",
      "id": "string",
      "stageId": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `boardId` | string | Associated board identifier. |
| `contactId` | string | Associated contact identifier. |
| `id` | string | CRM ticket identifier. |
| `stageId` | string | Associated stage identifier. |
| `title` | string | CRM ticket title. |

## Native endpoint

Through the native ChatDaddy API, this operation is `POST /crm/tickets` (base URL `https://api.chatdaddy.tech/im`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-crm-ticket.md) for the provider-specific parameters and requirements.

