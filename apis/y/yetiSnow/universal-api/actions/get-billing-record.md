# Yeti Snow: Get Billing Record



```
GET https://connect.mindcloud.co/v1/universal/yetiSnow/latest/actions/get-billing-record
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Yeti Snow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/yetiSnow/latest/actions/get-billing-record?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/yetiSnow/latest/actions/get-billing-record?${params}`, {
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
| `billingRecordId` | string | no | Billing record identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "due_date": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "status": "string",
      "value": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `due_date` | date | Billing due date. |
| `id` | string | Billing record identifier. |
| `status` | string | Billing record status. |
| `value` | number | Billing amount. |

## Native endpoint

Through the native Yeti Snow API, this operation is `GET report/billing/show` (base URL `https://sandbox_api.yetisoftware.com/api/en/public_access/1715`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-billing-record.md) for the provider-specific parameters and requirements.

