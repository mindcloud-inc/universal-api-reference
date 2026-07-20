# Webex: Create Membership

Creates a new membership in Webex.

```
POST https://connect.mindcloud.co/v1/universal/webex/latest/actions/create-membership
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Webex `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/webex/latest/actions/create-membership" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "roomId": "Y2lzY29zcGFyazovL3VzL1JPT00v...",
  "personEmail": "apps@mindcloud.co"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/webex/latest/actions/create-membership', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "roomId": "Y2lzY29zcGFyazovL3VzL1JPT00v...",
    "personEmail": "apps@mindcloud.co"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `roomId` | string | yes | Room to add the member to. Example: `Y2lzY29zcGFyazovL3VzL1JPT00v...`. |
| `personEmail` | string | yes | Email address of the member to add. Example: `apps@mindcloud.co`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "isModerator": true,
      "isMonitor": true,
      "isRoomHidden": true,
      "personDisplayName": "Ava Chen",
      "personEmail": "ava@example.com",
      "personId": "string",
      "personOrgId": "string",
      "roomId": "string",
      "roomType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | date | Membership creation timestamp. |
| `id` | string | Membership identifier. |
| `isModerator` | boolean | Whether the member is a moderator. |
| `isMonitor` | boolean | Whether the member is a monitor. |
| `isRoomHidden` | boolean | Whether the room is hidden for the member. |
| `personDisplayName` | string | Display name for the member. |
| `personEmail` | string | Email address for the member. |
| `personId` | string | Person identifier for the member. |
| `personOrgId` | string | Organization identifier for the member. |
| `roomId` | string | Room associated with the membership. |
| `roomType` | string | Type of room associated with the membership. |

## Native endpoint

Through the native Webex API, this operation is `POST /memberships` (base URL `https://webexapis.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-membership.md) for the provider-specific parameters and requirements.

