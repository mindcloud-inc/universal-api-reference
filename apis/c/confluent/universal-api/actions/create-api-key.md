# Confluent: Create API Key

Creates a new API key in Confluent Cloud.

```
POST https://connect.mindcloud.co/v1/universal/confluent/latest/actions/create-api-key
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Confluent `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/confluent/latest/actions/create-api-key" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "spec.owner.id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/confluent/latest/actions/create-api-key', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "spec.owner.id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `spec.owner.id` | string | yes |  |
| `spec.displayName` | string | no |  |
| `spec.description` | string | no |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `spec.resource.id` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "apiVersion": "string",
      "id": "string",
      "kind": "string",
      "metadata": {},
      "spec": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `apiVersion` | string |  |
| `id` | string |  |
| `kind` | string |  |
| `metadata` | object |  |
| `spec` | object |  |

## Native endpoint

Through the native Confluent API, this operation is `POST /iam/v2/api-keys` (base URL `https://api.confluent.cloud`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-api-key.md) for the provider-specific parameters and requirements.

