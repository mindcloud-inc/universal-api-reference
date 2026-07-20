# Confluent: Read Role Binding

Retrieves a role binding from Confluent Cloud.

```
GET https://connect.mindcloud.co/v1/universal/confluent/latest/actions/read-role-binding
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Confluent `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/confluent/latest/actions/read-role-binding?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/confluent/latest/actions/read-role-binding?${params}`, {
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
      "crnPattern": "string",
      "id": "string",
      "kind": "string",
      "metadata": {},
      "principal": "string",
      "roleName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `apiVersion` | string |  |
| `crnPattern` | string |  |
| `id` | string |  |
| `kind` | string |  |
| `metadata` | object |  |
| `principal` | string |  |
| `roleName` | string |  |

## Native endpoint

Through the native Confluent API, this operation is `GET /iam/v2/role-bindings/:id` (base URL `https://api.confluent.cloud`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/read-role-binding.md) for the provider-specific parameters and requirements.

