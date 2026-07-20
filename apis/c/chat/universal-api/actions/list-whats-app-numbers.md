# 2Chat: List WhatsApp Numbers

Retrieves connected WhatsApp numbers from 2Chat.

```
GET https://connect.mindcloud.co/v1/universal/chat/latest/actions/list-whats-app-numbers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 2Chat `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chat/latest/actions/list-whats-app-numbers?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chat/latest/actions/list-whats-app-numbers?${params}`, {
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
| `status` | string | no | Filter numbers by status: connected, disconnected, or all. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "numbers": [
        {
          "channelType": "string",
          "connectionStatus": "string",
          "createdAt": "2026-05-07T12:00:00.000Z",
          "enabled": true,
          "friendlyName": "Ava Chen",
          "id": "string",
          "isBusinessProfile": true,
          "isoCountryCode": "string",
          "lang": "string",
          "phoneNumber": "string",
          "platform": {},
          "pushname": {},
          "server": {},
          "syncContacts": true,
          "timezone": "string",
          "timezonePhoneNumber": "string",
          "updatedAt": "2026-05-07T12:00:00.000Z",
          "uuid": "string"
        }
      ],
      "page": 1,
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number |  |
| `numbers[].channelType` | string |  |
| `numbers[].connectionStatus` | string |  |
| `numbers[].createdAt` | date |  |
| `numbers[].enabled` | boolean |  |
| `numbers[].friendlyName` | string |  |
| `numbers[].id` | string |  |
| `numbers[].isBusinessProfile` | boolean |  |
| `numbers[].isoCountryCode` | string |  |
| `numbers[].lang` | string |  |
| `numbers[].phoneNumber` | string |  |
| `numbers[].platform` | object |  |
| `numbers[].pushname` | object |  |
| `numbers[].server` | object |  |
| `numbers[].syncContacts` | boolean |  |
| `numbers[].timezone` | string |  |
| `numbers[].timezonePhoneNumber` | string |  |
| `numbers[].updatedAt` | date |  |
| `numbers[].uuid` | string |  |
| `page` | number |  |
| `success` | boolean |  |

## Native endpoint

Through the native 2Chat API, this operation is `GET /whatsapp/get-numbers` (base URL `https://api.p.2chat.io/open`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-whats-app-numbers.md) for the provider-specific parameters and requirements.

