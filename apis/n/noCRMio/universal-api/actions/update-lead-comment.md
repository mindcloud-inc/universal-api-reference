# noCRM.io: Update Lead Comment

Updates an existing lead comment in noCRM.io.

```
PUT https://connect.mindcloud.co/v1/universal/noCRMio/latest/actions/update-lead-comment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a noCRM.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/noCRMio/latest/actions/update-lead-comment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "leadId": "string",
  "id": "string",
  "content": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/noCRMio/latest/actions/update-lead-comment', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "leadId": "string",
    "id": "string",
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
| `id` | string | yes | Comment ID. |
| `content` | string | yes | Replacement comment content. |
| `activityId` | number | no | Activity ID to set on the comment. |
| `isPinned` | boolean | no | Whether the comment is pinned. |

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

Through the native noCRM.io API, this operation is `PUT /leads/:lead_id/comments/:id` (base URL `{{credentials.baseUrl}}/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-lead-comment.md) for the provider-specific parameters and requirements.

