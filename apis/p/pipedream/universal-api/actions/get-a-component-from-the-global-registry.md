# Pipedream: Get a component from the global registry

Retrieves a registry component from Pipedream by key.

```
GET https://connect.mindcloud.co/v1/universal/pipedream/latest/actions/get-a-component-from-the-global-registry
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pipedream `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pipedream/latest/actions/get-a-component-from-the-global-registry?connectionId=$CONNECTION_ID&componentKey=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "componentKey": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pipedream/latest/actions/get-a-component-from-the-global-registry?${params}`, {
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
| `componentKey` | string | yes | The registry component key. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": "string",
      "codeHash": "string",
      "configurableProps": [
        {}
      ],
      "createdAt": 1,
      "id": "string",
      "name": "Ava Chen",
      "updatedAt": 1,
      "version": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | string |  |
| `codeHash` | string |  |
| `configurableProps` | array<object> |  |
| `createdAt` | number |  |
| `id` | string |  |
| `name` | string |  |
| `updatedAt` | number |  |
| `version` | string |  |

## Native endpoint

Through the native Pipedream API, this operation is `GET /components/registry/{key}` (base URL `https://api.pipedream.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-a-component-from-the-global-registry.md) for the provider-specific parameters and requirements.

