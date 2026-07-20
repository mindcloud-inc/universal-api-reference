# 2Chat: List WhatsApp Groups

Retrieves WhatsApp groups from 2Chat.

```
GET https://connect.mindcloud.co/v1/universal/chat/latest/actions/list-whats-app-groups
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 2Chat `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chat/latest/actions/list-whats-app-groups?connectionId=$CONNECTION_ID&from_number=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "from_number": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chat/latest/actions/list-whats-app-groups?${params}`, {
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
| `from_number` | string | yes | The WhatsApp number connected to 2Chat whose groups you want to list. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "channelIsOwner": true,
          "channelUuid": "string",
          "createdAt": "2026-05-07T12:00:00.000Z",
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
      ],
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[].channelIsOwner` | boolean |  |
| `data[].channelUuid` | string |  |
| `data[].createdAt` | date |  |
| `data[].isMuted` | boolean |  |
| `data[].isReadOnly` | boolean |  |
| `data[].profilePicUrl` | object |  |
| `data[].size` | number |  |
| `data[].updatedAt` | date |  |
| `data[].uuid` | string |  |
| `data[].waCreatedAt` | date |  |
| `data[].waGroupId` | string |  |
| `data[].waGroupName` | string |  |
| `data[].waOwnerId` | string |  |
| `data[].waSubject` | object |  |
| `success` | boolean |  |

## Native endpoint

Through the native 2Chat API, this operation is `GET /whatsapp/groups/:from_number` (base URL `https://api.p.2chat.io/open`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-whats-app-groups.md) for the provider-specific parameters and requirements.

