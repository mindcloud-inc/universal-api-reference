# Zoho Desk: List Threads



```
GET https://connect.mindcloud.co/v1/universal/zohoDesk/latest/actions/list-threads
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Desk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoDesk/latest/actions/list-threads?connectionId=$CONNECTION_ID&ticketId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "ticketId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoDesk/latest/actions/list-threads?${params}`, {
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
| `ticketId` | string | yes | The Zoho Desk ticket ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attachmentCount": "string",
      "author": {},
      "canReply": true,
      "channel": "string",
      "contentType": "string",
      "createdTime": "2026-05-07T12:00:00.000Z",
      "direction": "string",
      "hasAttach": true,
      "id": "string",
      "isDescriptionThread": true,
      "status": "string",
      "summary": "string",
      "visibility": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attachmentCount` | string |  |
| `author` | object |  |
| `canReply` | boolean |  |
| `channel` | string |  |
| `contentType` | string |  |
| `createdTime` | date |  |
| `direction` | string |  |
| `hasAttach` | boolean |  |
| `id` | string |  |
| `isDescriptionThread` | boolean |  |
| `status` | string |  |
| `summary` | string |  |
| `visibility` | string |  |

## Native endpoint

Through the native Zoho Desk API, this operation is `GET /tickets/[:ticketId]/threads` (base URL `https://desk.zoho.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-threads.md) for the provider-specific parameters and requirements.

