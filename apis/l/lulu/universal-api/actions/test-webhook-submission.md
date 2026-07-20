# Lulu: Test Webhook Submission

Creates a test webhook submission in Lulu.

```
POST https://connect.mindcloud.co/v1/universal/lulu/latest/actions/test-webhook-submission
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lulu `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/lulu/latest/actions/test-webhook-submission" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "6b522ab9-31ec-4418-a904-95436160d4a8",
  "topic": "PRINT_JOB_STATUS_CHANGED"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/lulu/latest/actions/test-webhook-submission', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "6b522ab9-31ec-4418-a904-95436160d4a8",
    "topic": "PRINT_JOB_STATUS_CHANGED"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Lulu webhook ID. Default: `6b522ab9-31ec-4418-a904-95436160d4a8`. |
| `topic` | string | yes | Webhook topic to test. Default: `PRINT_JOB_STATUS_CHANGED`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |

## Native endpoint

Through the native Lulu API, this operation is `POST /webhooks/{id}/test-submission/{topic}/` (base URL `{{credentials.apiBaseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/test-webhook-submission.md) for the provider-specific parameters and requirements.

