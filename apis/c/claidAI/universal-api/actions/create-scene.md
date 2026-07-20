# Claid AI: Create Scene

Creates a scene in Claid AI.

```
POST https://connect.mindcloud.co/v1/universal/claidAI/latest/actions/create-scene
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Claid AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/claidAI/latest/actions/create-scene" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "object": {},
  "scene": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/claidAI/latest/actions/create-scene', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "object": {},
    "scene": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `object` | object | yes |  |
| `output` | string | no | Example: `storage://storage_1/output/`. |
| `scene` | object | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "input": {},
      "output": [
        {}
      ],
      "profiling": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `input` | object | Input scene request metadata. |
| `output` | array<object> | Generated scene outputs. |
| `profiling` | object | Execution profiling details. |

## Native endpoint

Through the native Claid AI API, this operation is `POST scene/create` (base URL `https://api.claid.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-scene.md) for the provider-specific parameters and requirements.

