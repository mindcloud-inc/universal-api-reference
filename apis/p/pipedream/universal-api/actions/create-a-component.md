# Pipedream: Create a component

Creates a new component in Pipedream.

```
POST https://connect.mindcloud.co/v1/universal/pipedream/latest/actions/create-a-component
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pipedream `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pipedream/latest/actions/create-a-component" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pipedream/latest/actions/create-a-component', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `componentCode` | string | no | The full Pipedream component code. |
| `componentUrl` | string | no | A URL reference to the hosted component source. |

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

Through the native Pipedream API, this operation is `POST /components` (base URL `https://api.pipedream.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-a-component.md) for the provider-specific parameters and requirements.

