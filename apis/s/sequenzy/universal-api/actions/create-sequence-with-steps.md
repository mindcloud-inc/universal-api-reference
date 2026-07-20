# Sequenzy: Create Sequence with Steps

Creates a sequence with explicit steps in Sequenzy.

```
POST https://connect.mindcloud.co/v1/universal/sequenzy/latest/actions/create-sequence-with-steps
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sequenzy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sequenzy/latest/actions/create-sequence-with-steps" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "eventName": "Ava Chen",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sequenzy/latest/actions/create-sequence-with-steps', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "eventName": "Ava Chen",
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `eventName` | string | yes | Trigger event name. |
| `name` | string | yes | Sequence name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "sequence": {
        "emailCount": 1,
        "id": "string",
        "name": "Ava Chen",
        "nodeCount": 1,
        "status": "string"
      },
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |
| `sequence.emailCount` | number |  |
| `sequence.id` | string |  |
| `sequence.name` | string |  |
| `sequence.nodeCount` | number |  |
| `sequence.status` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Sequenzy API, this operation is `POST /sequences` (base URL `https://api.sequenzy.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-sequence-with-steps.md) for the provider-specific parameters and requirements.

