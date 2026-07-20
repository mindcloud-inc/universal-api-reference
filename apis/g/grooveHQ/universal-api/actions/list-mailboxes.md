# GrooveHQ: List Mailboxes

Retrieves mailboxes from GrooveHQ.

```
GET https://connect.mindcloud.co/v1/universal/grooveHQ/latest/actions/list-mailboxes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GrooveHQ `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/grooveHQ/latest/actions/list-mailboxes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/grooveHQ/latest/actions/list-mailboxes?${params}`, {
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
      "channelType": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "forwardEmailAddress": "ava@example.com",
      "id": "string",
      "links": {},
      "name": "Ava Chen",
      "preferences": {},
      "restrictionType": "string",
      "senderName": "Ava Chen",
      "state": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `channelType` | string | Mailbox channel type. |
| `createdAt` | date | Mailbox creation timestamp. |
| `forwardEmailAddress` | string | Groove forwarding address for the mailbox. |
| `id` | string | Mailbox identifier. |
| `links` | object | Provider links for related mailbox resources. |
| `name` | string | Mailbox display name. |
| `preferences` | object | Mailbox preference settings. |
| `restrictionType` | string | Mailbox visibility restriction. |
| `senderName` | string | Sender name used by the mailbox. |
| `state` | string | Mailbox state. |

## Native endpoint

Through the native GrooveHQ API, this operation is `GET /mailboxes` (base URL `https://api.groovehq.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-mailboxes.md) for the provider-specific parameters and requirements.

