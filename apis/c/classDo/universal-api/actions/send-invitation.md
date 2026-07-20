# ClassDo: Send Invitation

Creates a new invitation in ClassDo.

```
POST https://connect.mindcloud.co/v1/universal/classDo/latest/actions/send-invitation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ClassDo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/classDo/latest/actions/send-invitation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "query": "mutation SendInvitation { sendInvitation(data: { roomId: \"ROOM_ID\", locale: En, contactInfo: \"student@example.com\", contactType: Email, contactFullName: \"Student Example\", organizationMemberRoleId: \"cmnfzfn5u2p6j08104tdj7jk2\" }) { id status } }"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/classDo/latest/actions/send-invitation', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "query": "mutation SendInvitation { sendInvitation(data: { roomId: \"ROOM_ID\", locale: En, contactInfo: \"student@example.com\", contactType: Email, contactFullName: \"Student Example\", organizationMemberRoleId: \"cmnfzfn5u2p6j08104tdj7jk2\" }) { id status } }"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `query` | string | yes | GraphQL mutation payload. Default: `mutation SendInvitation { sendInvitation(data: { roomId: \"ROOM_ID\", locale: En, contactInfo: \"student@example.com\", contactType: Email, contactFullName: \"Student Example\", organizationMemberRoleId: \"cmnfzfn5u2p6j08104tdj7jk2\" }) { id status } }`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "sendInvitation": {
          "id": "string",
          "status": "string"
        }
      },
      "errors": [
        {
          "message": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.sendInvitation.id` | string |  |
| `data.sendInvitation.status` | string |  |
| `errors[].message` | string |  |

## Native endpoint

Through the native ClassDo API, this operation is `POST /graphql` (base URL `https://api.classdo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-invitation.md) for the provider-specific parameters and requirements.

