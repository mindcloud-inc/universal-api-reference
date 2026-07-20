# Zoho Connect: Add Event Invitees

Adds invitees to an event in Zoho Connect.

```
POST https://connect.mindcloud.co/v1/universal/zohoConnect/latest/actions/add-event-invitees
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Connect `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zohoConnect/latest/actions/add-event-invitees" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "scopeId": "string",
  "streamId": "string",
  "invitedMembers": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoConnect/latest/actions/add-event-invitees', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "scopeId": "string",
    "streamId": "string",
    "invitedMembers": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `scopeId` | string | yes |  |
| `streamId` | string | yes |  |
| `invitedMembers` | string | yes | Accepts multiple values in one string, delimited by `,`. |
| `invitedGroups` | string | no | Accepts multiple values in one string, delimited by `,`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "addEventInvitees": {
        "invitedUserList": [
          {}
        ],
        "result": "string",
        "sharedUserList": [
          {}
        ]
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `addEventInvitees.invitedUserList` | array<object> |  |
| `addEventInvitees.result` | string |  |
| `addEventInvitees.sharedUserList` | array<object> |  |

## Native endpoint

Through the native Zoho Connect API, this operation is `POST /pulse/api/addEventInvitees` (base URL `https://connect.zoho.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-event-invitees.md) for the provider-specific parameters and requirements.

