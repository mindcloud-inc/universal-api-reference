# Visma eAccounting: Get Customer

Retrieves a customer from Visma eAccounting.

```
GET https://connect.mindcloud.co/v1/universal/vismaEAccounting/latest/actions/get-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Visma eAccounting `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vismaEAccounting/latest/actions/get-customer?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vismaEAccounting/latest/actions/get-customer?${params}`, {
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
      "changedUtc": "2026-05-07T12:00:00.000Z",
      "currencyCode": "string",
      "customerNumber": "string",
      "emailAddress": "ava@example.com",
      "id": "string",
      "invoiceCity": "string",
      "invoicePostalCode": "string",
      "name": "Ava Chen",
      "vatNumber": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `changedUtc` | date |  |
| `currencyCode` | string |  |
| `customerNumber` | string |  |
| `emailAddress` | string |  |
| `id` | string |  |
| `invoiceCity` | string |  |
| `invoicePostalCode` | string |  |
| `name` | string |  |
| `vatNumber` | string |  |

## Native endpoint

Through the native Visma eAccounting API, this operation is `GET /customers/{customerId}` (base URL `https://eaccountingapi.vismaonline.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-customer.md) for the provider-specific parameters and requirements.

