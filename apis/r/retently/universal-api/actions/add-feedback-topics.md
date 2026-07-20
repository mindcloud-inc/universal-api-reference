# Retently: Add Feedback Topics

Updates topics on a feedback response in Retently.

```
PUT https://connect.mindcloud.co/v1/universal/retently/latest/actions/add-feedback-topics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Retently `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/retently/latest/actions/add-feedback-topics" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "topics[].name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/retently/latest/actions/add-feedback-topics', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "topics[].name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Response ID; |
| `topics[]` | array<object> | no | An array of topic objects |
| `topics[].name` | string | yes | The topic name |
| `topics[].sentiment` | string | no | The sentiment of the topic (if not provided, defaults to 'neutral') |
| `op` | string | no | Use the flag âappendâ in order to append the topics to the response, or leave it empty in order to override existing topics assigned to the response; |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number |  |
| `message` | string |  |

## Native endpoint

Through the native Retently API, this operation is `POST /api/v2/response/topics` (base URL `https://app.retently.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-feedback-topics.md) for the provider-specific parameters and requirements.

