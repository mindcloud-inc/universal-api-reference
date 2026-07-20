# Stormboard: Invite Participants

Invites participants to a Storm in Stormboard.

```
POST https://connect.mindcloud.co/v1/universal/stormboard/latest/actions/invite-participants
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stormboard `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/stormboard/latest/actions/invite-participants" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "participants[]": [
    "string"
  ],
  "stormId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/stormboard/latest/actions/invite-participants', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "participants[]": ["string"],
    "stormId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `message` | string | no | Optional custom message to send with the invite. |
| `participants[]` | array<string> | yes | Array of email addresses to invite. |
| `permissionType` | string | no | Permission for invited users: contributor or viewer. |
| `stormId` | number | yes | Storm ID from the Stormboard share dialog or related storm record. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "invited": 1,
      "message": "string",
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `invited` | number |  |
| `message` | string |  |
| `status` | number |  |

## Native endpoint

Through the native Stormboard API, this operation is `POST /storms/:storm_id/invite` (base URL `https://api.stormboard.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/invite-participants.md) for the provider-specific parameters and requirements.

