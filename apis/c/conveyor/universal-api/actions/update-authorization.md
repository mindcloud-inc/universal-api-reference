# Conveyor: Update Authorization

Updates or revokes an authorization in Conveyor.

```
PUT https://connect.mindcloud.co/v1/universal/conveyor/latest/actions/update-authorization
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Conveyor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/conveyor/latest/actions/update-authorization" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "authorizationId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/conveyor/latest/actions/update-authorization', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "authorizationId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `authorizationId` | string | yes | Authorization identifier. |
| `status` | string | no | Authorization status; Conveyor documents revocation with `revoked`. |
| `accessGroupIds[]` | array<string> | no | Access group identifiers. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_embedded": {
        "access_groups": [
          {
            "id": "string",
            "name": "Ava Chen"
          }
        ]
      },
      "_links": {},
      "_type": "string",
      "connection_id": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "dataroom_id": "string",
      "email": "ava@example.com",
      "gate_document_signature_id": "string",
      "id": "string",
      "is_owner": true,
      "status": "string",
      "subscribed": true,
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_embedded` | object |  |
| `_embedded.access_groups` | array<object> |  |
| `_embedded.access_groups[].id` | string |  |
| `_embedded.access_groups[].name` | string |  |
| `_links` | object |  |
| `_type` | string |  |
| `connection_id` | string |  |
| `created_at` | date |  |
| `dataroom_id` | string |  |
| `email` | string |  |
| `gate_document_signature_id` | string |  |
| `id` | string |  |
| `is_owner` | boolean |  |
| `status` | string |  |
| `subscribed` | boolean |  |
| `updated_at` | date |  |

## Native endpoint

Through the native Conveyor API, this operation is `PATCH /v2/exchange/authorizations/:authorization_id` (base URL `https://api.conveyor.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-authorization.md) for the provider-specific parameters and requirements.

