# Qlik: Create Space

Creates a new space in your Qlik tenant.

```
POST https://connect.mindcloud.co/v1/universal/qlik/latest/actions/create-space
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Qlik `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/qlik/latest/actions/create-space" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Analytics Workspace",
  "type": "shared"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/qlik/latest/actions/create-space', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Analytics Workspace",
    "type": "shared"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Space name. Example: `Analytics Workspace`. |
| `type` | string | yes | Space type. Example: `shared`. |
| `description` | string | no | Space description. Example: `Workspace for analytics apps`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "id": "string",
      "name": "Ava Chen",
      "ownerId": "string",
      "tenantId": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string |  |
| `id` | string |  |
| `name` | string |  |
| `ownerId` | string |  |
| `tenantId` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Qlik API, this operation is `POST /api/v1/spaces` (base URL `https://{{credentials.tenantHost}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-space.md) for the provider-specific parameters and requirements.

