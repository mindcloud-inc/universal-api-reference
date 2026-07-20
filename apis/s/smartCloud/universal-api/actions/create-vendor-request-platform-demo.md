# 2Smart Cloud: Request platform demo



```
POST https://connect.mindcloud.co/v1/universal/smartCloud/latest/actions/create-vendor-request-platform-demo
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 2Smart Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/smartCloud/latest/actions/create-vendor-request-platform-demo" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "message": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/smartCloud/latest/actions/create-vendor-request-platform-demo', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "message": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | user name |
| `message` | string | yes | Message describing request |

## Response

```json
{
  "success": true,
  "data": [
    {
      "completed": true,
      "created": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "message": "string",
      "name": "Ava Chen",
      "updated": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `completed` | boolean |  |
| `created` | date |  |
| `id` | number |  |
| `message` | string |  |
| `name` | string |  |
| `updated` | date |  |

## Native endpoint

Through the native 2Smart Cloud API, this operation is `POST /vendor/request-platform-demo` (base URL `https://cloud.2smart.com/robot/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-vendor-request-platform-demo.md) for the provider-specific parameters and requirements.

