# ManyChat: Update Subscriber

Updates an existing subscriber in ManyChat.

```
PUT https://connect.mindcloud.co/v1/universal/manyChat/latest/actions/update-subscriber
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ManyChat `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/manyChat/latest/actions/update-subscriber" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "subscriber_id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/manyChat/latest/actions/update-subscriber', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "subscriber_id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `subscriber_id` | number | yes |  |
| `first_name` | string | no |  |
| `last_name` | string | no |  |
| `phone` | string | no |  |
| `email` | string | no |  |
| `gender` | string | no |  |
| `has_opt_in_sms` | boolean | no |  |
| `has_opt_in_email` | boolean | no |  |
| `consent_phrase` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "customFields": [
        {
          "description": "string",
          "id": 1,
          "name": "Ava Chen",
          "type": "string",
          "value": "string"
        }
      ],
      "email": "ava@example.com",
      "firstName": "Ava",
      "gender": "string",
      "id": "string",
      "igId": {},
      "igLastInteraction": {},
      "igLastSeen": {},
      "igUsername": {},
      "isFollowupEnabled": true,
      "language": {},
      "lastInputText": {},
      "lastInteraction": {},
      "lastName": "Chen",
      "lastSeen": {},
      "liveChatUrl": "https://example.com",
      "locale": {},
      "name": "Ava Chen",
      "optinEmail": true,
      "optinPhone": true,
      "optinWhatsapp": true,
      "pageId": "string",
      "phone": "string",
      "profilePic": {},
      "status": "string",
      "subscribed": "string",
      "tags": [
        {
          "id": 1,
          "name": "Ava Chen"
        }
      ],
      "timezone": "string",
      "whatsappPhone": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `customFields[].description` | string |  |
| `customFields[].id` | number |  |
| `customFields[].name` | string |  |
| `customFields[].type` | string |  |
| `customFields[].value` | string |  |
| `email` | string |  |
| `firstName` | string |  |
| `gender` | string |  |
| `id` | string |  |
| `igId` | object |  |
| `igLastInteraction` | object |  |
| `igLastSeen` | object |  |
| `igUsername` | object |  |
| `isFollowupEnabled` | boolean |  |
| `language` | object |  |
| `lastInputText` | object |  |
| `lastInteraction` | object |  |
| `lastName` | string |  |
| `lastSeen` | object |  |
| `liveChatUrl` | string |  |
| `locale` | object |  |
| `name` | string |  |
| `optinEmail` | boolean |  |
| `optinPhone` | boolean |  |
| `optinWhatsapp` | boolean |  |
| `pageId` | string |  |
| `phone` | string |  |
| `profilePic` | object |  |
| `status` | string |  |
| `subscribed` | string |  |
| `tags[].id` | number |  |
| `tags[].name` | string |  |
| `timezone` | string |  |
| `whatsappPhone` | object |  |

## Native endpoint

Through the native ManyChat API, this operation is `POST /fb/subscriber/updateSubscriber` (base URL `https://api.manychat.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-subscriber.md) for the provider-specific parameters and requirements.

