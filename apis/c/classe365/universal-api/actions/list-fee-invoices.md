# Classe365: List Fee Invoices

Retrieves a list of fee invoices from Classe365.

```
GET https://connect.mindcloud.co/v1/universal/classe365/latest/actions/list-fee-invoices
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Classe365 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/classe365/latest/actions/list-fee-invoices?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/classe365/latest/actions/list-fee-invoices?${params}`, {
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
      "amount": 1,
      "invoiceId": 1,
      "invoiceNumber": "string",
      "studentId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number |  |
| `invoiceId` | number |  |
| `invoiceNumber` | string |  |
| `studentId` | number |  |

## Native endpoint

Through the native Classe365 API, this operation is `GET /rest/feeInvoicesData` (base URL `https://{{credentials.username}}.classe365.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-fee-invoices.md) for the provider-specific parameters and requirements.

