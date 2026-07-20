# Bigjpg: Create Enlarge Task

Creates an image enlargement task in Bigjpg.

```
POST https://connect.mindcloud.co/v1/universal/bigjpg/latest/actions/create-enlarge-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bigjpg `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/bigjpg/latest/actions/create-enlarge-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "input": "https://example.com/image.jpg",
  "style": "art",
  "noise": "3",
  "x2": "1"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bigjpg/latest/actions/create-enlarge-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "input": "https://example.com/image.jpg",
    "style": "art",
    "noise": "3",
    "x2": "1"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `input` | string | yes | Public URL of the image to enlarge. Example: `https://example.com/image.jpg`. |
| `style` | list | yes | Bigjpg image style: art for illustrations or photo for photographs. One of: `art`, `photo`. Default: `art`. |
| `noise` | list | yes | Noise reduction level documented by Bigjpg. One of: `-1`, `0`, `1`, `2`, `3`. Default: `3`. |
| `x2` | list | yes | Upscale factor selector documented by Bigjpg. One of: `1`, `2`, `3`, `4`. Default: `1`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fileName` | string | no | Optional file name from the Bigjpg Python example. Example: `small.jpg`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "status": "string",
      "tid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `status` | string | Bigjpg task creation status or business gating message. |
| `tid` | string | Bigjpg task ID returned when an enlarge task is accepted. |

## Native endpoint

Through the native Bigjpg API, this operation is `POST /task/` (base URL `https://bigjpg.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-enlarge-task.md) for the provider-specific parameters and requirements.

