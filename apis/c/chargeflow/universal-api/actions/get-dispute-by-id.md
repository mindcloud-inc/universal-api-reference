# Chargeflow: Get Dispute By ID

Retrieves an existing dispute from Chargeflow.

```
GET https://connect.mindcloud.co/v1/universal/chargeflow/latest/actions/get-dispute-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chargeflow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chargeflow/latest/actions/get-dispute-by-id?connectionId=$CONNECTION_ID&disputeId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "disputeId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chargeflow/latest/actions/get-dispute-by-id?${params}`, {
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
| `disputeId` | string | yes | The Chargeflow dispute ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "account_id": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "ext_account_id": "string",
      "id": "string",
      "source": "string",
      "source_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account_id` | string |  |
| `created_at` | date |  |
| `ext_account_id` | string |  |
| `id` | string |  |
| `source` | string |  |
| `source_id` | string |  |

## Native endpoint

Through the native Chargeflow API, this operation is `GET /disputes/{disputeId}` (base URL `https://api.chargeflow.io/public/2025-04-01`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-dispute-by-id.md) for the provider-specific parameters and requirements.

