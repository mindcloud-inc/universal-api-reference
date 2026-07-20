# SweetProcess: Create Invitation

Creates a new invitation in SweetProcess.

```
POST https://connect.mindcloud.co/v1/universal/sweetProcess/latest/actions/create-invitation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SweetProcess `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sweetProcess/latest/actions/create-invitation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "invitations[].contentType": "team",
  "invitations[].permission": "view",
  "invitations[].objectId": 1,
  "invitations[].toUserId": "https://www.sweetprocess.com/api/v1/users/32010/"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sweetProcess/latest/actions/create-invitation', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "invitations[].contentType": "team",
    "invitations[].permission": "view",
    "invitations[].objectId": 1,
    "invitations[].toUserId": "https://www.sweetprocess.com/api/v1/users/32010/"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `invitations[]` | array<object> | no | One or more invitation objects to send to SweetProcess. |
| `invitations[].sendMail` | boolean | no | Whether SweetProcess should send an email for this invitation row. Default: `false`. |
| `invitations[].contentType` | string | yes | The target object type for the invitation, for example team. Default: `team`. |
| `invitations[].permission` | string | yes | The permission level to assign, for example view. Default: `view`. |
| `invitations[].objectId` | number | yes | The numeric ID of the referenced team or document. |
| `invitations[].toUserId` | string | yes | The SweetProcess user API URL that should receive the invitation. Example: `https://www.sweetprocess.com/api/v1/users/32010/`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contentType": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "fromUser": {},
      "id": 1,
      "objectId": 1,
      "permission": "string",
      "sharedItem": {},
      "status": "string",
      "toUser": {},
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contentType` | string | The shared object type, for example team. |
| `createdAt` | date | When the invitation was created. |
| `fromUser` | object | The user who created the invitation. |
| `id` | number | The numeric SweetProcess invitation ID. |
| `objectId` | number | The numeric ID of the shared target object. |
| `permission` | string | The permission granted by the invitation. |
| `sharedItem` | object | The shared SweetProcess object referenced by the invitation. |
| `status` | string | The invitation status, for example pending. |
| `toUser` | object | The invited SweetProcess user. |
| `url` | string | The API URL for the invitation. |

## Native endpoint

Through the native SweetProcess API, this operation is `POST /invitations/` (base URL `https://www.sweetprocess.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-invitation.md) for the provider-specific parameters and requirements.

