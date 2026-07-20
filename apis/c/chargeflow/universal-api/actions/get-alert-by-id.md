# Chargeflow: Get Alert By ID

Retrieves an existing alert from Chargeflow.

```
GET https://connect.mindcloud.co/v1/universal/chargeflow/latest/actions/get-alert-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chargeflow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chargeflow/latest/actions/get-alert-by-id?connectionId=$CONNECTION_ID&alertId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "alertId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chargeflow/latest/actions/get-alert-by-id?${params}`, {
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
| `alertId` | string | yes | The Chargeflow alert ID. |

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
      "network_transaction": {
        "amount": 1,
        "id": "string"
      }
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
| `network_transaction.amount` | number |  |
| `network_transaction.id` | string |  |

## Native endpoint

Through the native Chargeflow API, this operation is `GET /alerts/{alertId}` (base URL `https://api.chargeflow.io/public/2025-04-01`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-alert-by-id.md) for the provider-specific parameters and requirements.

