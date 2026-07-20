# Pipedream: Get a component

Retrieves a component from Pipedream by ID or key.

```
GET https://connect.mindcloud.co/v1/universal/pipedream/latest/actions/get-a-component
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pipedream `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pipedream/latest/actions/get-a-component?connectionId=$CONNECTION_ID&componentIdOrKey=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "componentIdOrKey": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pipedream/latest/actions/get-a-component?${params}`, {
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
| `componentIdOrKey` | string | yes | The component ID or key. |

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

Through the native Pipedream API, this operation is `GET /components/{key|id}` (base URL `https://api.pipedream.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-a-component.md) for the provider-specific parameters and requirements.

