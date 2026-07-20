# Emailable: Get Batch Status

Retrieves the status of a batch from Emailable.

```
GET https://connect.mindcloud.co/v1/universal/emailable/latest/actions/get-batch-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Emailable `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/emailable/latest/actions/get-batch-status?connectionId=$CONNECTION_ID&batchId=5cf6dd30093f96d2ac34bb0a" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "batchId": "5cf6dd30093f96d2ac34bb0a"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/emailable/latest/actions/get-batch-status?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `batchId` | string | yes | The batch ID returned when you created the verification batch. Example: `5cf6dd30093f96d2ac34bb0a`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `partial` | boolean | no | Set to true to include partial results while a batch of up to 1,000 emails is still verifying. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "emails": [
        {
          "email": "ava@example.com",
          "score": 1,
          "state": "ava@example.com"
        }
      ],
      "id": "string",
      "message": "string",
      "reasonCounts": {
        "acceptedEmail": 1,
        "invalidDomain": 1,
        "invalidEmail": 1,
        "invalidSmtp": 1,
        "lowDeliverability": 1,
        "lowQuality": 1,
        "noConnect": 1,
        "rejectedEmail": 1,
        "timeout": 1,
        "unavailableSmtp": 1,
        "unexpectedError": 1
      },
      "totalCounts": {
        "deliverable": 1,
        "duplicate": 1,
        "processed": 1,
        "risky": 1,
        "total": 1,
        "undeliverable": 1,
        "unknown": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `emails[].email` | string |  |
| `emails[].score` | number |  |
| `emails[].state` | string |  |
| `id` | string |  |
| `message` | string |  |
| `reasonCounts.acceptedEmail` | number |  |
| `reasonCounts.invalidDomain` | number |  |
| `reasonCounts.invalidEmail` | number |  |
| `reasonCounts.invalidSmtp` | number |  |
| `reasonCounts.lowDeliverability` | number |  |
| `reasonCounts.lowQuality` | number |  |
| `reasonCounts.noConnect` | number |  |
| `reasonCounts.rejectedEmail` | number |  |
| `reasonCounts.timeout` | number |  |
| `reasonCounts.unavailableSmtp` | number |  |
| `reasonCounts.unexpectedError` | number |  |
| `totalCounts.deliverable` | number |  |
| `totalCounts.duplicate` | number |  |
| `totalCounts.processed` | number |  |
| `totalCounts.risky` | number |  |
| `totalCounts.total` | number |  |
| `totalCounts.undeliverable` | number |  |
| `totalCounts.unknown` | number |  |

## Native endpoint

Through the native Emailable API, this operation is `GET /v1/batch` (base URL `https://api.emailable.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-batch-status.md) for the provider-specific parameters and requirements.

