# EZ Texting: List Messages

Retrieves messages from EZ Texting.

```
GET https://connect.mindcloud.co/v1/universal/eZTexting/latest/actions/list-messages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EZ Texting `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eZTexting/latest/actions/list-messages?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eZTexting/latest/actions/list-messages?${params}`, {
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
| `filters[contactNumber][eq]` | string | no | Filter messages by contact number Example: `(737) 337-8315`. |
| `filters[deleted][eq]` | string | no | Filter messages by deleted state |
| `filters[group][eq]` | string | no | Filter messages by group |
| `filters[incoming][eq]` | string | no | Filter messages by incoming state |
| `filters[messageId][eq]` | string | no | Filter messages by message ID |
| `filters[optType][eq]` | string | no | Filter messages by opt type |
| `filters[pending][eq]` | string | no | Filter messages by pending state |
| `filters[sentAt][gte]` | string | no | Filter messages sent at or after this time |
| `filters[sentAt][lte]` | string | no | Filter messages sent at or before this time |
| `filters[textQuery][eq]` | string | no | Filter messages by text query |
| `filters[type][eq]` | string | no | Filter messages by type |
| `filters[unread][eq]` | string | no | Filter messages by unread state |
| `filters[userNumber][eq]` | string | no | Filter messages by user number Example: `(737) 337-8315`. |
| `page` | number | no | Page offset starting at 0 |
| `size` | number | no | Page size |
| `sort` | string | no | Sort field and direction |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contactNumber": "string",
      "group": true,
      "id": "string",
      "inbound": true,
      "mediaUrl": "https://example.com",
      "message": "string",
      "messageGroupId": "string",
      "optIn": true,
      "optOut": true,
      "sentAt": "2026-05-07T12:00:00.000Z",
      "status": "string",
      "type": "string",
      "userNumber": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contactNumber` | string |  |
| `group` | boolean |  |
| `id` | string |  |
| `inbound` | boolean |  |
| `mediaUrl` | string |  |
| `message` | string |  |
| `messageGroupId` | string |  |
| `optIn` | boolean |  |
| `optOut` | boolean |  |
| `sentAt` | date |  |
| `status` | string |  |
| `type` | string |  |
| `userNumber` | string |  |

## Native endpoint

Through the native EZ Texting API, this operation is `GET /messages` (base URL `https://a.eztexting.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-messages.md) for the provider-specific parameters and requirements.

