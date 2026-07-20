# Infisical: Update Secret

Updates an existing secret in a project environment in Infisical.

```
PUT https://connect.mindcloud.co/v1/universal/infisical/latest/actions/update-secret
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Infisical `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/infisical/latest/actions/update-secret" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "secretName": "Ava Chen",
  "projectId": "string",
  "environment": "string",
  "secretValue": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/infisical/latest/actions/update-secret', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "secretName": "Ava Chen",
    "projectId": "string",
    "environment": "string",
    "secretValue": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `secretName` | string | yes |  |
| `projectId` | string | yes |  |
| `environment` | string | yes |  |
| `secretValue` | string | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Infisical API returns.

## Native endpoint

Through the native Infisical API, this operation is `PATCH /api/v4/secrets/:secretName` (base URL `https://app.infisical.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-secret.md) for the provider-specific parameters and requirements.

