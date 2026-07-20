# Escrow.com: Get Transaction Timeline Entries

Retrieves transaction timeline entries from Escrow.com.

```
GET https://connect.mindcloud.co/v1/universal/escrowcom/latest/actions/get-transaction-timeline-entries
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Escrow.com `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/escrowcom/latest/actions/get-transaction-timeline-entries?connectionId=$CONNECTION_ID&transactionId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "transactionId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/escrowcom/latest/actions/get-transaction-timeline-entries?${params}`, {
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
| `transactionId` | number | yes | The Escrow.com transaction ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "dateAdded": "2026-05-07T12:00:00.000Z",
      "notes": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dateAdded` | date | Timestamp when the timeline entry was added. |
| `notes` | string | Timeline note text. |

## Native endpoint

Through the native Escrow.com API, this operation is `GET /transaction/:transaction_id/timeline-entries` (base URL `https://api.escrow-sandbox.com/2017-09-01`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-transaction-timeline-entries.md) for the provider-specific parameters and requirements.

