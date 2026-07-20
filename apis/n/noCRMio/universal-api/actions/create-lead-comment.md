# noCRM.io: Create Lead Comment

Creates a new lead comment in noCRM.io.

```
POST https://connect.mindcloud.co/v1/universal/noCRMio/latest/actions/create-lead-comment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a noCRM.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/noCRMio/latest/actions/create-lead-comment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "leadId": "string",
  "content": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/noCRMio/latest/actions/create-lead-comment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "leadId": "string",
    "content": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `leadId` | string | yes | Lead ID. |
| `content` | string | yes | Comment content. |
| `userId` | string | no | User email or ID for comment ownership. |
| `attachments` | list<object> | no | Attachments to add on the comment. |
| `activityId` | number | no | Activity ID to set on the comment. |
| `createdAt` | date | no | Override comment creation date. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "actionItem": {},
      "activity": {},
      "activityId": {},
      "attachments": [
        [
          "string"
        ]
      ],
      "commentedItem": {
        "id": 1,
        "item": "string"
      },
      "content": "string",
      "createdAt": "string",
      "extendedInfo": {},
      "id": 1,
      "isPinned": true,
      "rawContent": "string",
      "reactions": [
        [
          "string"
        ]
      ],
      "user": {
        "email": "ava@example.com",
        "firstname": "Ava",
        "id": 1,
        "lastname": "Chen",
        "mobilePhone": {},
        "phone": {}
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `actionItem` | object |  |
| `activity` | object |  |
| `activityId` | object |  |
| `attachments[]` | array<string> |  |
| `commentedItem` | object |  |
| `commentedItem.id` | number |  |
| `commentedItem.item` | string |  |
| `content` | string |  |
| `createdAt` | string |  |
| `extendedInfo` | object |  |
| `id` | number |  |
| `isPinned` | boolean |  |
| `rawContent` | string |  |
| `reactions[]` | array<string> |  |
| `user` | object |  |
| `user.email` | string |  |
| `user.firstname` | string |  |
| `user.id` | number |  |
| `user.lastname` | string |  |
| `user.mobilePhone` | object |  |
| `user.phone` | object |  |

## Native endpoint

Through the native noCRM.io API, this operation is `POST /leads/:lead_id/comments` (base URL `{{credentials.baseUrl}}/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-lead-comment.md) for the provider-specific parameters and requirements.

