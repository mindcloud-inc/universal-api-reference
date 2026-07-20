# Kickbox: Start Batch Verification

Starts a batch email verification job in Kickbox.

```
POST https://connect.mindcloud.co/v1/universal/kickbox/latest/actions/start-batch-verification
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kickbox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/kickbox/latest/actions/start-batch-verification" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "emails": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kickbox/latest/actions/start-batch-verification', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "emails": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `emails` | string | yes | Plain-text or CSV body content containing one email address per line. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "message": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number | Kickbox batch verification job ID. |
| `message` | string | Provider message returned when the batch job is created. |
| `success` | boolean | Whether the batch verification job was accepted by Kickbox. |

## Native endpoint

Through the native Kickbox API, this operation is `PUT /verify-batch` (base URL `https://api.kickbox.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/start-batch-verification.md) for the provider-specific parameters and requirements.

