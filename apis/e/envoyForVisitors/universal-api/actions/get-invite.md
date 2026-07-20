# Envoy for Visitors: Get Invite

Retrieves an invite from Envoy for Visitors.

```
GET https://connect.mindcloud.co/v1/universal/envoyForVisitors/latest/actions/get-invite
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Envoy for Visitors `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/envoyForVisitors/latest/actions/get-invite?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/envoyForVisitors/latest/actions/get-invite?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "approvalStatus": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "customFields": [
        {}
      ],
      "expectedArrivalAt": "2026-05-07T12:00:00.000Z",
      "expectedDepartureAt": "2026-05-07T12:00:00.000Z",
      "flowId": "string",
      "host": {},
      "id": "string",
      "invitee": {},
      "locationId": "string",
      "notes": "string",
      "photoUrl": "https://example.com",
      "recurringInviteId": "string",
      "secretToken": "string",
      "sendEmailToInvitee": true,
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `approvalStatus` | string |  |
| `createdAt` | date |  |
| `customFields` | array<object> |  |
| `expectedArrivalAt` | date |  |
| `expectedDepartureAt` | date |  |
| `flowId` | string |  |
| `host` | object |  |
| `id` | string |  |
| `invitee` | object |  |
| `locationId` | string |  |
| `notes` | string |  |
| `photoUrl` | string |  |
| `recurringInviteId` | string |  |
| `secretToken` | string |  |
| `sendEmailToInvitee` | boolean |  |
| `type` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Envoy for Visitors API, this operation is `GET /invites/:id` (base URL `https://api.envoy.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-invite.md) for the provider-specific parameters and requirements.

