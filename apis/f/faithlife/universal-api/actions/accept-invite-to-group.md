# Faithlife: Accept Invite To Group

Accepts a group invite in Faithlife.

```
POST https://connect.mindcloud.co/v1/universal/faithlife/latest/actions/accept-invite-to-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Faithlife `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/faithlife/latest/actions/accept-invite-to-group" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "inviteId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/faithlife/latest/actions/accept-invite-to-group', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "inviteId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `inviteId` | string | yes | The pending Faithlife invite ID to accept. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "membershipId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `membershipId` | string |  |

## Native endpoint

Through the native Faithlife API, this operation is `POST /invites/:inviteId/accept` (base URL `https://accountsapi.logos.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/accept-invite-to-group.md) for the provider-specific parameters and requirements.

