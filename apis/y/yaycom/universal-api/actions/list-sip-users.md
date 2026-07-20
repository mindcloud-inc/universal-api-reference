# Yay.com: List SIP Users

Retrieves SIP users from Yay.com.

```
GET https://connect.mindcloud.co/v1/universal/yaycom/latest/actions/list-sip-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Yay.com `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/yaycom/latest/actions/list-sip-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/yaycom/latest/actions/list-sip-users?${params}`, {
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
      "allowDirectCalls": true,
      "allowedCallerIds": [
        "string"
      ],
      "allowMultiDevice": true,
      "callEncryption": true,
      "callerId": "string",
      "callRecording": true,
      "canAutoDeploy": true,
      "canBarge": true,
      "canBeBarged": true,
      "canBeListened": true,
      "canBePickedUp": true,
      "canBeWhispered": true,
      "canInviteAnonymously": true,
      "canListen": true,
      "canPickup": true,
      "canWhisper": true,
      "chatEnabled": true,
      "countryCode": "string",
      "displayName": "Ava Chen",
      "emergencyCallerId": "string",
      "extension": 1,
      "holdPlaylist": "string",
      "mobileDnd": true,
      "mobileDndAllowInternal": true,
      "muteChatNotifications": true,
      "personalMailbox": "string",
      "relatedProduct": "string",
      "restrictCallerId": true,
      "restrictOutbound": true,
      "ringDuration": 1,
      "showMissedCalls": true,
      "timezone": "string",
      "transferBackupExtension": 1,
      "type": 1,
      "useDefaultPlaylist": true,
      "useDirectCalls": true,
      "useMailboxOnTransfer": true,
      "userName": "Ava Chen",
      "userPassword": "string",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `allowDirectCalls` | boolean |  |
| `allowedCallerIds` | array<string> |  |
| `allowMultiDevice` | boolean |  |
| `callEncryption` | boolean |  |
| `callerId` | string |  |
| `callRecording` | boolean |  |
| `canAutoDeploy` | boolean |  |
| `canBarge` | boolean |  |
| `canBeBarged` | boolean |  |
| `canBeListened` | boolean |  |
| `canBePickedUp` | boolean |  |
| `canBeWhispered` | boolean |  |
| `canInviteAnonymously` | boolean |  |
| `canListen` | boolean |  |
| `canPickup` | boolean |  |
| `canWhisper` | boolean |  |
| `chatEnabled` | boolean |  |
| `countryCode` | string |  |
| `displayName` | string |  |
| `emergencyCallerId` | string |  |
| `extension` | number |  |
| `holdPlaylist` | string |  |
| `mobileDnd` | boolean |  |
| `mobileDndAllowInternal` | boolean |  |
| `muteChatNotifications` | boolean |  |
| `personalMailbox` | string |  |
| `relatedProduct` | string |  |
| `restrictCallerId` | boolean |  |
| `restrictOutbound` | boolean |  |
| `ringDuration` | number |  |
| `showMissedCalls` | boolean |  |
| `timezone` | string |  |
| `transferBackupExtension` | number |  |
| `type` | number |  |
| `useDefaultPlaylist` | boolean |  |
| `useDirectCalls` | boolean |  |
| `useMailboxOnTransfer` | boolean |  |
| `userName` | string |  |
| `userPassword` | string |  |
| `uuid` | string |  |

## Native endpoint

Through the native Yay.com API, this operation is `GET /voip/user` (base URL `https://api.yay.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-sip-users.md) for the provider-specific parameters and requirements.

