# QuickFile: Search Payments



```
GET https://connect.mindcloud.co/v1/universal/quickFile/latest/actions/search-payments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a QuickFile `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/quickFile/latest/actions/search-payments?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/quickFile/latest/actions/search-payments?${params}`, {
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
| `limit` | number | no | Default: `2`. |
| `offset` | number | no | Default: `0`. |
| `dateFrom` | date | no | Default: `2000-01-01`. |
| `dateTo` | date | no | Default: `2030-12-31`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "notes": "string",
      "paymentDate": "2026-05-07T12:00:00.000Z",
      "paymentId": 1,
      "paymentMethod": "string",
      "reference": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number | Payment amount. |
| `notes` | string | Payment notes. |
| `paymentDate` | date | Date the payment was recorded. |
| `paymentId` | number | QuickFile payment identifier. |
| `paymentMethod` | string | Payment method used. |
| `reference` | string | Provider payment reference. |

## Native endpoint

Through the native QuickFile API, this operation is `POST /payment/search` (base URL `https://api.quickfile.co.uk/1_2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-payments.md) for the provider-specific parameters and requirements.

