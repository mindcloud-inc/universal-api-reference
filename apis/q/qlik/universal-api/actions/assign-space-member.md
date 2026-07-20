# Qlik: Assign Space Member

Assigns a user or group to a space in Qlik.

```
POST https://connect.mindcloud.co/v1/universal/qlik/latest/actions/assign-space-member
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Qlik `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/qlik/latest/actions/assign-space-member" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "spaceId": "65b8f2a1f4b0c2d3e4f56789",
  "type": "user",
  "roles[]": "consumer",
  "assigneeId": "65b8f2a1f4b0c2d3e4f56789"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/qlik/latest/actions/assign-space-member', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "spaceId": "65b8f2a1f4b0c2d3e4f56789",
    "type": "user",
    "roles[]": "consumer",
    "assigneeId": "65b8f2a1f4b0c2d3e4f56789"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `spaceId` | string | yes | Qlik space ID. Example: `65b8f2a1f4b0c2d3e4f56789`. |
| `type` | string | yes | Assignment assignee type, such as user or group. Example: `user`. |
| `roles[]` | array<string> | yes | Roles to grant in the space assignment. Example: `consumer`. |
| `assigneeId` | string | yes | User or group ID to assign to the space. Example: `65b8f2a1f4b0c2d3e4f56789`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assigneeId": "string",
      "id": "string",
      "roles": [
        [
          "string"
        ]
      ],
      "spaceId": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assigneeId` | string |  |
| `id` | string |  |
| `roles[]` | array<string> |  |
| `spaceId` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Qlik API, this operation is `POST /api/v1/spaces/:spaceId/assignments` (base URL `https://{{credentials.tenantHost}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/assign-space-member.md) for the provider-specific parameters and requirements.

