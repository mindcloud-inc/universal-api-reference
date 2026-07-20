# 2Chat: List Conversations

Retrieves WhatsApp conversations from 2Chat for a channel.

```
GET https://connect.mindcloud.co/v1/universal/chat/latest/actions/list-conversations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 2Chat `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chat/latest/actions/list-conversations?connectionId=$CONNECTION_ID&channel_uuid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "channel_uuid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chat/latest/actions/list-conversations?${params}`, {
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
| `channel_uuid` | string | yes | The UUID of the WhatsApp channel connected to 2Chat. |
| `pageNumber` | number | no | Zero-based page number for older conversation pages. Default: `0`. |
| `phoneNumber` | string | no | Filter conversations by digits contained in the phone number. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "pageNumber": 1,
      "sessions": [
        {
          "channelUuid": "string",
          "createdAt": "2026-05-07T12:00:00.000Z",
          "device": {},
          "friendlyName": {},
          "isGroupChat": true,
          "isoCountryCode": "string",
          "lastActivityAt": "2026-05-07T12:00:00.000Z",
          "lastUserMessageSentAt": "2026-05-07T12:00:00.000Z",
          "phoneNumber": "string",
          "profilePicUrl": {},
          "regionName": "Ava Chen",
          "sessionKey": "string",
          "timezone": "string",
          "whatsappGroup": {
            "channelIsOwner": true,
            "channelUuid": "string",
            "createdAt": "2026-05-07T12:00:00.000Z",
            "inviteCode": "string",
            "inviteLink": "https://example.com",
            "isMuted": true,
            "isReadOnly": true,
            "profilePicUrl": {},
            "size": 1,
            "updatedAt": "2026-05-07T12:00:00.000Z",
            "uuid": "string",
            "waCreatedAt": "2026-05-07T12:00:00.000Z",
            "waGroupId": "string",
            "waGroupName": "Ava Chen",
            "waOwnerId": "string",
            "waSubject": {}
          }
        }
      ],
      "success": true,
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `pageNumber` | number |  |
| `sessions[].channelUuid` | string |  |
| `sessions[].createdAt` | date |  |
| `sessions[].device` | object |  |
| `sessions[].friendlyName` | object |  |
| `sessions[].isGroupChat` | boolean |  |
| `sessions[].isoCountryCode` | string |  |
| `sessions[].lastActivityAt` | date |  |
| `sessions[].lastUserMessageSentAt` | date |  |
| `sessions[].phoneNumber` | string |  |
| `sessions[].profilePicUrl` | object |  |
| `sessions[].regionName` | string |  |
| `sessions[].sessionKey` | string |  |
| `sessions[].timezone` | string |  |
| `sessions[].whatsappGroup.channelIsOwner` | boolean |  |
| `sessions[].whatsappGroup.channelUuid` | string |  |
| `sessions[].whatsappGroup.createdAt` | date |  |
| `sessions[].whatsappGroup.inviteCode` | string |  |
| `sessions[].whatsappGroup.inviteLink` | string |  |
| `sessions[].whatsappGroup.isMuted` | boolean |  |
| `sessions[].whatsappGroup.isReadOnly` | boolean |  |
| `sessions[].whatsappGroup.profilePicUrl` | object |  |
| `sessions[].whatsappGroup.size` | number |  |
| `sessions[].whatsappGroup.updatedAt` | date |  |
| `sessions[].whatsappGroup.uuid` | string |  |
| `sessions[].whatsappGroup.waCreatedAt` | date |  |
| `sessions[].whatsappGroup.waGroupId` | string |  |
| `sessions[].whatsappGroup.waGroupName` | string |  |
| `sessions[].whatsappGroup.waOwnerId` | string |  |
| `sessions[].whatsappGroup.waSubject` | object |  |
| `success` | boolean |  |
| `total` | number |  |

## Native endpoint

Through the native 2Chat API, this operation is `GET /whatsapp/conversations/:channel_uuid` (base URL `https://api.p.2chat.io/open`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-conversations.md) for the provider-specific parameters and requirements.

