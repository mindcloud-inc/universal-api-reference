# Tarvent: List Account Invoices

Retrieves account invoices from Tarvent.

```
GET https://connect.mindcloud.co/v1/universal/tarvent/latest/actions/list-account-invoices
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tarvent `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tarvent/latest/actions/list-account-invoices?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tarvent/latest/actions/list-account-invoices?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "billPeriodEndUtc": "2026-05-07T12:00:00.000Z",
      "billPeriodStartUtc": "2026-05-07T12:00:00.000Z",
      "dueUtc": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "status": "string",
      "totalAmount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `billPeriodEndUtc` | date |  |
| `billPeriodStartUtc` | date |  |
| `dueUtc` | date |  |
| `id` | string |  |
| `status` | string |  |
| `totalAmount` | number |  |

## Native endpoint

Through the native Tarvent API, this operation is `POST /graphql` (base URL `https://api.tarvent.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-account-invoices.md) for the provider-specific parameters and requirements.

