# Kit: Add Subscriber to Sequence

Adds an existing subscriber to a Kit sequence.

```
POST https://connect.mindcloud.co/v1/universal/kit/latest/actions/add-subscriber-to-sequence
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/kit/latest/actions/add-subscriber-to-sequence" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "sequenceId": "12345",
  "emailAddress": "subscriber@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kit/latest/actions/add-subscriber-to-sequence', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "sequenceId": "12345",
    "emailAddress": "subscriber@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sequenceId` | number | yes | The ID of the sequence to add the subscriber to. Example: `12345`. |
| `emailAddress` | string | yes | Email address of an existing subscriber. Example: `subscriber@example.com`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Kit API returns.

## Native endpoint

Through the native Kit API, this operation is `POST /sequences/:sequence_id/subscribers` (base URL `https://api.kit.com/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-subscriber-to-sequence.md) for the provider-specific parameters and requirements.

