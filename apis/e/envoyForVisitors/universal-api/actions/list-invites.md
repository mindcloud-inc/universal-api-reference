# Envoy for Visitors: List Invites

Finds invites in Envoy for Visitors.

```
GET https://connect.mindcloud.co/v1/universal/envoyForVisitors/latest/actions/list-invites
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Envoy for Visitors `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/envoyForVisitors/latest/actions/list-invites?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/envoyForVisitors/latest/actions/list-invites?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



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

Through the native Envoy for Visitors API, this operation is `GET /invites` (base URL `https://api.envoy.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-invites.md) for the provider-specific parameters and requirements.

