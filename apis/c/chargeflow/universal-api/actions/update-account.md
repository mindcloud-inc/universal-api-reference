# Chargeflow: Update Account

Updates an existing Chargeflow Connect account.

```
PUT https://connect.mindcloud.co/v1/universal/chargeflow/latest/actions/update-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chargeflow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/chargeflow/latest/actions/update-account" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "accountId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chargeflow/latest/actions/update-account', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "accountId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `accountId` | string | yes | The Chargeflow account ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "business_name": "Ava Chen",
      "business_url": "https://example.com",
      "created_at": "2026-05-07T12:00:00.000Z",
      "ext_account_id": "string",
      "id": "string",
      "owner_name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `business_name` | string |  |
| `business_url` | string |  |
| `created_at` | date |  |
| `ext_account_id` | string |  |
| `id` | string |  |
| `owner_name` | string |  |

## Native endpoint

Through the native Chargeflow API, this operation is `PATCH /accounts/{accountId}` (base URL `https://api.chargeflow.io/public/2025-04-01`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-account.md) for the provider-specific parameters and requirements.

