# Chargback: Get Alert

Retrieves detailed alert records from Chargback.

```
GET https://connect.mindcloud.co/v1/universal/chargback/latest/actions/get-alert
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chargback `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chargback/latest/actions/get-alert?connectionId=$CONNECTION_ID&external_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "external_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chargback/latest/actions/get-alert?${params}`, {
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
| `external_id` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "alert_id": "string",
      "alert_service": "string",
      "alert_status": "string",
      "amount": "string",
      "created_at": "string",
      "currency": "string",
      "external_id": "string",
      "is_demo": true,
      "updated_at": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `alert_id` | string | Provider alert identifier. |
| `alert_service` | string | Source service for the alert. |
| `alert_status` | string | Current alert status. |
| `amount` | string | Original alert amount. |
| `created_at` | string | Alert creation timestamp. |
| `currency` | string | Currency for the original amount. |
| `external_id` | string | Chargeback alert external identifier. |
| `is_demo` | boolean | Whether the alert belongs to demo data. |
| `updated_at` | string | Alert last update timestamp. |

## Native endpoint

Through the native Chargback API, this operation is `GET /api/public/v1/alerts/:external_id/` (base URL `https://api.chargeback.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-alert.md) for the provider-specific parameters and requirements.

