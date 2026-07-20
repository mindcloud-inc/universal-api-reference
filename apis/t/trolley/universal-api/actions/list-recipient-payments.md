# Trolley: List Recipient Payments

Retrieves payments for a recipient from Trolley.

```
GET https://connect.mindcloud.co/v1/universal/trolley/latest/actions/list-recipient-payments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Trolley `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/trolley/latest/actions/list-recipient-payments?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/trolley/latest/actions/list-recipient-payments?${params}`, {
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
| `id` | string | no | Recipient ID |

## Response

```json
{
  "success": true,
  "data": [
    {
      "meta": {},
      "ok": true,
      "payments": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `meta` | object |  |
| `ok` | boolean |  |
| `payments` | array<object> |  |

## Native endpoint

Through the native Trolley API, this operation is `GET /v1/recipients/:id/payments` (base URL `https://api.trolley.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-recipient-payments.md) for the provider-specific parameters and requirements.

