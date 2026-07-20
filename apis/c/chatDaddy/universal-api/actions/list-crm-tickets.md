# ChatDaddy: List CRM Tickets

Retrieves CRM ticket records from ChatDaddy.

```
GET https://connect.mindcloud.co/v1/universal/chatDaddy/latest/actions/list-crm-tickets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ChatDaddy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chatDaddy/latest/actions/list-crm-tickets?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chatDaddy/latest/actions/list-crm-tickets?${params}`, {
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
| `count` | number | no | Number of CRM tickets to return. |
| `nextPageCursor` | string | no | Cursor for the next CRM ticket page. |

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
| `boardId` | string |  |
| `contactId` | string |  |
| `id` | string |  |
| `stageId` | string |  |
| `title` | string |  |

## Native endpoint

Through the native ChatDaddy API, this operation is `GET /crm/tickets` (base URL `https://api.chatdaddy.tech/im`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-crm-tickets.md) for the provider-specific parameters and requirements.

