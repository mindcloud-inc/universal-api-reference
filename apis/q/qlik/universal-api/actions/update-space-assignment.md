# Qlik: Update Space Assignment

Updates an existing space assignment in Qlik.

```
PUT https://connect.mindcloud.co/v1/universal/qlik/latest/actions/update-space-assignment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Qlik `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/qlik/latest/actions/update-space-assignment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "spaceId": "65b8f2a1f4b0c2d3e4f56789",
  "assignmentId": "65b8f2a1f4b0c2d3e4f56789",
  "roles[]": "consumer"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/qlik/latest/actions/update-space-assignment', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "spaceId": "65b8f2a1f4b0c2d3e4f56789",
    "assignmentId": "65b8f2a1f4b0c2d3e4f56789",
    "roles[]": "consumer"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `spaceId` | string | yes | Qlik space ID. Example: `65b8f2a1f4b0c2d3e4f56789`. |
| `assignmentId` | string | yes | Qlik space assignment ID. Example: `65b8f2a1f4b0c2d3e4f56789`. |
| `roles[]` | array<string> | yes | Replacement roles for the assignment. Example: `consumer`. |

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

Through the native Qlik API, this operation is `PUT /api/v1/spaces/:spaceId/assignments/:assignmentId` (base URL `https://{{credentials.tenantHost}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-space-assignment.md) for the provider-specific parameters and requirements.

