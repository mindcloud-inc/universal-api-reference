# Intruder: Update Target API Schema



```
PUT https://connect.mindcloud.co/v1/universal/intruder/latest/actions/update-target-api-schema
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Intruder `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/intruder/latest/actions/update-target-api-schema" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "targetId": "string",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/intruder/latest/actions/update-target-api-schema', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "targetId": "string",
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `targetId` | string | yes | Target ID. |
| `id` | string | yes | API schema ID. |
| `baseUrl` | string | no | Base URL for the API schema. |
| `name` | string | no | API schema name. |
| `targetAuthenticationId` | number | no | Related target authentication ID. |
| `file` | file | no | API schema file upload. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "baseUrl": "https://example.com",
      "id": 1,
      "name": "Ava Chen",
      "targetAuthenticationId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `baseUrl` | string |  |
| `id` | number |  |
| `name` | string |  |
| `targetAuthenticationId` | number |  |

## Native endpoint

Through the native Intruder API, this operation is `PATCH /targets/:target_id/api_schemas/:id/` (base URL `https://api.intruder.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-target-api-schema.md) for the provider-specific parameters and requirements.

