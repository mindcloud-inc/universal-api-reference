# PiAPI/Trellis: Create Trellis Text-to-3D Task

Creates a Trellis text-to-3D task in PiAPI/Trellis.

```
POST https://connect.mindcloud.co/v1/universal/piAPITrellis/latest/actions/create-trellis-text-to-3d-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PiAPI/Trellis `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/piAPITrellis/latest/actions/create-trellis-text-to-3d-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "input.prompt": "a bear"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/piAPITrellis/latest/actions/create-trellis-text-to-3d-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "input.prompt": "a bear"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `input.prompt` | string | yes | Prompt describing the 3D object to generate. Example: `a bear`. |
| `input.seed` | number | no | Optional random seed. Example: `0`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native PiAPI/Trellis API returns.

## Native endpoint

Through the native PiAPI/Trellis API, this operation is `POST /api/v1/task` (base URL `https://api.piapi.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-trellis-text-to-3d-task.md) for the provider-specific parameters and requirements.

