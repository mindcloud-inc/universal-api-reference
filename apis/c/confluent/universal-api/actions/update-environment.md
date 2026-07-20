# Confluent: Update Environment

Updates an existing environment in Confluent Cloud.

```
PUT https://connect.mindcloud.co/v1/universal/confluent/latest/actions/update-environment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Confluent `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/confluent/latest/actions/update-environment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/confluent/latest/actions/update-environment', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes |  |
| `displayName` | string | no |  |
| `streamGovernanceConfig.package` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "apiVersion": "string",
      "displayName": "Ava Chen",
      "id": "string",
      "kind": "string",
      "metadata": {},
      "streamGovernanceConfig": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `apiVersion` | string |  |
| `displayName` | string |  |
| `id` | string |  |
| `kind` | string |  |
| `metadata` | object |  |
| `streamGovernanceConfig` | object |  |

## Native endpoint

Through the native Confluent API, this operation is `PATCH /org/v2/environments/:id` (base URL `https://api.confluent.cloud`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-environment.md) for the provider-specific parameters and requirements.

