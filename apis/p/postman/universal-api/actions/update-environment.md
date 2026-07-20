# Postman: Update Environment

Updates an existing environment in Postman.

```
PUT https://connect.mindcloud.co/v1/universal/postman/latest/actions/update-environment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Postman `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/postman/latest/actions/update-environment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "environmentId": "string",
  "patch.op": "string",
  "patch.path": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/postman/latest/actions/update-environment', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "environmentId": "string",
    "patch.op": "string",
    "patch.path": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `environmentId` | string | yes | The environment's ID. |
| `patch.op` | string | yes |  |
| `patch.path` | string | yes |  |
| `patch.value` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "environment": {
        "id": "string",
        "name": "Ava Chen",
        "uid": "string",
        "updatedAt": "2026-05-07T12:00:00.000Z"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `environment.id` | string |  |
| `environment.name` | string |  |
| `environment.uid` | string |  |
| `environment.updatedAt` | date |  |

## Native endpoint

Through the native Postman API, this operation is `PATCH /environments/:environmentId` (base URL `https://api.getpostman.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-environment.md) for the provider-specific parameters and requirements.

