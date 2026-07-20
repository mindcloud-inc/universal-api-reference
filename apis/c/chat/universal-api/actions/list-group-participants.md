# 2Chat: List Group Participants

Retrieves WhatsApp group participants from 2Chat.

```
GET https://connect.mindcloud.co/v1/universal/chat/latest/actions/list-group-participants
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 2Chat `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chat/latest/actions/list-group-participants?connectionId=$CONNECTION_ID&group_uuid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "group_uuid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chat/latest/actions/list-group-participants?${params}`, {
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
| `group_uuid` | string | yes | The UUID of the WhatsApp group. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "channelIsOwner": true,
        "channelUuid": "string",
        "createdAt": "2026-05-07T12:00:00.000Z",
        "inviteCode": "string",
        "inviteLink": "https://example.com",
        "isMuted": true,
        "isReadOnly": true,
        "ownerData": {
          "formattedPhoneNumber": "string",
          "isoCountryCode": "string",
          "phoneNumber": "string"
        },
        "participants": [
          {
            "createdAt": "2026-05-07T12:00:00.000Z",
            "device": {},
            "formattedPhoneNumber": "string",
            "id": "string",
            "isoCountryCode": "string",
            "phoneNumber": "string",
            "profilePicUrl": {},
            "updatedAt": "2026-05-07T12:00:00.000Z",
            "waIsAdmin": true,
            "waIsSuperAdmin": true,
            "waParticipantId": "string",
            "waPushname": {}
          }
        ],
        "profilePicUrl": {},
        "size": 1,
        "updatedAt": "2026-05-07T12:00:00.000Z",
        "uuid": "string",
        "waCreatedAt": "2026-05-07T12:00:00.000Z",
        "waGroupId": "string",
        "waGroupName": "Ava Chen",
        "waOwnerId": "string",
        "waSubject": {}
      },
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.channelIsOwner` | boolean |  |
| `data.channelUuid` | string |  |
| `data.createdAt` | date |  |
| `data.inviteCode` | string |  |
| `data.inviteLink` | string |  |
| `data.isMuted` | boolean |  |
| `data.isReadOnly` | boolean |  |
| `data.ownerData.formattedPhoneNumber` | string |  |
| `data.ownerData.isoCountryCode` | string |  |
| `data.ownerData.phoneNumber` | string |  |
| `data.participants[].createdAt` | date |  |
| `data.participants[].device` | object |  |
| `data.participants[].formattedPhoneNumber` | string |  |
| `data.participants[].id` | string |  |
| `data.participants[].isoCountryCode` | string |  |
| `data.participants[].phoneNumber` | string |  |
| `data.participants[].profilePicUrl` | object |  |
| `data.participants[].updatedAt` | date |  |
| `data.participants[].waIsAdmin` | boolean |  |
| `data.participants[].waIsSuperAdmin` | boolean |  |
| `data.participants[].waParticipantId` | string |  |
| `data.participants[].waPushname` | object |  |
| `data.profilePicUrl` | object |  |
| `data.size` | number |  |
| `data.updatedAt` | date |  |
| `data.uuid` | string |  |
| `data.waCreatedAt` | date |  |
| `data.waGroupId` | string |  |
| `data.waGroupName` | string |  |
| `data.waOwnerId` | string |  |
| `data.waSubject` | object |  |
| `success` | boolean |  |

## Native endpoint

Through the native 2Chat API, this operation is `GET /whatsapp/group/:group_uuid` (base URL `https://api.p.2chat.io/open`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-group-participants.md) for the provider-specific parameters and requirements.

