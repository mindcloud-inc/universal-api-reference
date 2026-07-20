# Qlik: Update Space Properties

Updates an existing space's properties in Qlik.

```
PUT https://connect.mindcloud.co/v1/universal/qlik/latest/actions/update-space-properties
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Qlik `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/qlik/latest/actions/update-space-properties" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "spaceId": "65b8f2a1f4b0c2d3e4f56789",
  "operations[]": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/qlik/latest/actions/update-space-properties', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "spaceId": "65b8f2a1f4b0c2d3e4f56789",
    "operations[]": "[object Object]"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `spaceId` | string | yes | Qlik space ID. Example: `65b8f2a1f4b0c2d3e4f56789`. |
| `operations[]` | array<object> | yes | JSON Patch operations array for updating the space. Example: `[object Object]`. |

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

Through the native Qlik API, this operation is `PATCH /api/v1/spaces/:spaceId` (base URL `https://{{credentials.tenantHost}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-space-properties.md) for the provider-specific parameters and requirements.

