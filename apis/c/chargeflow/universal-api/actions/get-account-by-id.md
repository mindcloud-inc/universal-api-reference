# Chargeflow: Get Account By ID

Retrieves an existing Chargeflow Connect account.

```
GET https://connect.mindcloud.co/v1/universal/chargeflow/latest/actions/get-account-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chargeflow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chargeflow/latest/actions/get-account-by-id?connectionId=$CONNECTION_ID&accountId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accountId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chargeflow/latest/actions/get-account-by-id?${params}`, {
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

Through the native Chargeflow API, this operation is `GET /accounts/{accountId}` (base URL `https://api.chargeflow.io/public/2025-04-01`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-account-by-id.md) for the provider-specific parameters and requirements.

