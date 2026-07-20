# FuseDesk: List Chats

Retrieves active chats from your FuseDesk account.

```
GET https://connect.mindcloud.co/v1/universal/fuseDesk/latest/actions/list-chats
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FuseDesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fuseDesk/latest/actions/list-chats?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fuseDesk/latest/actions/list-chats?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "caseId": 1,
      "clientName": "Ava Chen",
      "contactId": 1,
      "contactUuid": "string",
      "dateClosed": "2026-05-07T12:00:00.000Z",
      "dateCreated": "2026-05-07T12:00:00.000Z",
      "dateLastMessage": "2026-05-07T12:00:00.000Z",
      "dateLastMessageReceived": "2026-05-07T12:00:00.000Z",
      "dateLastResponse": "2026-05-07T12:00:00.000Z",
      "departmentId": 1,
      "id": "string",
      "isArchived": true,
      "lastMessage": "string",
      "lastMessageSender": "string",
      "noteId": 1,
      "platform": "string",
      "repId": 1,
      "title": "string",
      "unseen": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `caseId` | number |  |
| `clientName` | string |  |
| `contactId` | number |  |
| `contactUuid` | string |  |
| `dateClosed` | date |  |
| `dateCreated` | date |  |
| `dateLastMessage` | date |  |
| `dateLastMessageReceived` | date |  |
| `dateLastResponse` | date |  |
| `departmentId` | number |  |
| `id` | string |  |
| `isArchived` | boolean |  |
| `lastMessage` | string |  |
| `lastMessageSender` | string |  |
| `noteId` | number |  |
| `platform` | string |  |
| `repId` | number |  |
| `title` | string |  |
| `unseen` | number |  |

## Native endpoint

Through the native FuseDesk API, this operation is `GET /api/v1/chats` (base URL `https://{{credentials.appName}}.fusedesk.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-chats.md) for the provider-specific parameters and requirements.

