# LoopedIn: Update Feedback

Updates an existing feedback item in LoopedIn.

```
PUT https://connect.mindcloud.co/v1/universal/loopedIn/latest/actions/update-feedback
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LoopedIn `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/loopedIn/latest/actions/update-feedback" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "category": "string",
  "id": "string",
  "title": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/loopedIn/latest/actions/update-feedback', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "category": "string",
    "id": "string",
    "title": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `category` | string | yes | The LoopedIn feedback category ID. |
| `id` | string | yes | The LoopedIn feedback ID. |
| `title` | string | yes | The updated feedback title. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true,
      "updated": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean |  |
| `updated` | boolean |  |

## Native endpoint

Through the native LoopedIn API, this operation is `PUT /feedback/:id` (base URL `https://api.loopedin.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-feedback.md) for the provider-specific parameters and requirements.

