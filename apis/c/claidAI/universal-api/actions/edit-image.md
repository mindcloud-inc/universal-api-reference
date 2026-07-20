# Claid AI: Edit Image

Creates an edited image in Claid AI.

```
POST https://connect.mindcloud.co/v1/universal/claidAI/latest/actions/edit-image
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Claid AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/claidAI/latest/actions/edit-image" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "input": "storage://storage_1/input/image.jpg",
  "operations": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/claidAI/latest/actions/edit-image', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "input": "storage://storage_1/input/image.jpg",
    "operations": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `input` | string | yes | Example: `storage://storage_1/input/image.jpg`. |
| `operations` | object | yes |  |
| `output` | string | no | Example: `storage://storage_1/output/`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "input": {},
      "output": {},
      "profiling": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `input` | object | Input image metadata. |
| `output` | object | Processed image metadata. |
| `profiling` | object | Execution profiling details. |

## Native endpoint

Through the native Claid AI API, this operation is `POST image/edit` (base URL `https://api.claid.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/edit-image.md) for the provider-specific parameters and requirements.

