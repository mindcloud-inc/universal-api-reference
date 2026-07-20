# Confluent: Read Environment

Retrieves an environment from Confluent Cloud.

```
GET https://connect.mindcloud.co/v1/universal/confluent/latest/actions/read-environment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Confluent `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/confluent/latest/actions/read-environment?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/confluent/latest/actions/read-environment?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes |  |

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

Through the native Confluent API, this operation is `GET /org/v2/environments/:id` (base URL `https://api.confluent.cloud`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/read-environment.md) for the provider-specific parameters and requirements.

