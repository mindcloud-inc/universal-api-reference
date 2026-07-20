# SpreadsheetWeb Hub: Create Workspace Invite

Creates a new workspace invite in SpreadsheetWeb Hub.

```
POST https://connect.mindcloud.co/v1/universal/spreadsheetWebHub/latest/actions/create-workspace-invite
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SpreadsheetWeb Hub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/spreadsheetWebHub/latest/actions/create-workspace-invite" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/spreadsheetWebHub/latest/actions/create-workspace-invite', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `request` | object | no | Primary request payload. |
| `request.workspaceId` | string | no | SpreadsheetWeb workspace UUID. |
| `request.email` | string | no | Invitee email address. |
| `request.message` | string | no | Optional invite message. |
| `request.userTemplateId` | string | no | Template user UUID applied to the invite. |
| `request.externalLoginProvider` | number | no | External login provider enum value. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "value": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `value` | boolean |  |

## Native endpoint

Through the native SpreadsheetWeb Hub API, this operation is `POST /invites/create` (base URL `https://api.spreadsheetweb.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-workspace-invite.md) for the provider-specific parameters and requirements.

