# Redbooth: Create Comment

Creates a new comment in Redbooth.

```
POST https://connect.mindcloud.co/v1/universal/redbooth/latest/actions/create-comment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Redbooth `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/redbooth/latest/actions/create-comment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "targetId": 1,
  "targetType": "string",
  "body": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/redbooth/latest/actions/create-comment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "targetId": 1,
    "targetType": "string",
    "body": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `targetId` | number | yes | Target object ID |
| `targetType` | string | yes | Target object type |
| `body` | string | yes | Comment body |

## Response

```json
{
  "success": true,
  "data": [
    {
      "body": "string",
      "id": 1,
      "project_id": 1,
      "status": "string",
      "target_id": 1,
      "target_type": "string",
      "type": "string",
      "user_id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `body` | string |  |
| `id` | number |  |
| `project_id` | number |  |
| `status` | string |  |
| `target_id` | number |  |
| `target_type` | string |  |
| `type` | string |  |
| `user_id` | number |  |

## Native endpoint

Through the native Redbooth API, this operation is `POST /comments` (base URL `https://redbooth.com/api/3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-comment.md) for the provider-specific parameters and requirements.

