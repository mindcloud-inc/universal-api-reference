# ChatDaddy: Delete CRM Ticket

Deletes an existing CRM ticket from ChatDaddy.

```
DELETE https://connect.mindcloud.co/v1/universal/chatDaddy/latest/actions/delete-crm-ticket
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ChatDaddy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/chatDaddy/latest/actions/delete-crm-ticket?connectionId=$CONNECTION_ID&id=sample-ticket-id" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "sample-ticket-id"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chatDaddy/latest/actions/delete-crm-ticket?${params}`, {
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
| `id` | string | yes | CRM ticket identifier to delete. Default: `sample-ticket-id`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean | Whether the CRM ticket deletion request completed successfully. |

## Native endpoint

Through the native ChatDaddy API, this operation is `DELETE /crm/tickets/{id}` (base URL `https://api.chatdaddy.tech/im`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-crm-ticket.md) for the provider-specific parameters and requirements.

