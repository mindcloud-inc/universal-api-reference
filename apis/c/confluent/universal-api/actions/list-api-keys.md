# Confluent: List API Keys

Retrieves API keys from Confluent Cloud.

```
GET https://connect.mindcloud.co/v1/universal/confluent/latest/actions/list-api-keys
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Confluent `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/confluent/latest/actions/list-api-keys?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/confluent/latest/actions/list-api-keys?${params}`, {
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
| `spec.owner` | string | no |  |
| `spec.resource` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "apiVersion": "string",
      "data": [
        {
          "id": "string",
          "spec": {}
        }
      ],
      "kind": "string",
      "metadata": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `apiVersion` | string |  |
| `data` | array<object> |  |
| `data[].id` | string |  |
| `data[].spec` | object |  |
| `kind` | string |  |
| `metadata` | object |  |

## Native endpoint

Through the native Confluent API, this operation is `GET /iam/v2/api-keys` (base URL `https://api.confluent.cloud`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-api-keys.md) for the provider-specific parameters and requirements.

