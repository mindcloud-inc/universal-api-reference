# Printful: Create Mockup Task

Creates a mockup generation task in Printful.

```
POST https://connect.mindcloud.co/v1/universal/printful/latest/actions/create-mockup-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Printful `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/printful/latest/actions/create-mockup-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "1"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/printful/latest/actions/create-mockup-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "1"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The Printful product variant id to generate mockups for. Default: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "mockups": [
        {}
      ],
      "status": "string",
      "task_key": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `mockups` | array<object> |  |
| `status` | string |  |
| `task_key` | string |  |

## Native endpoint

Through the native Printful API, this operation is `POST /mockup-generator/create-task/{id}` (base URL `https://api.printful.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-mockup-task.md) for the provider-specific parameters and requirements.

