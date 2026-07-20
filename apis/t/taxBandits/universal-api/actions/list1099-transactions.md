# TaxBandits: List 1099 Transactions

Retrieves 1099 transactions from TaxBandits.

```
GET https://connect.mindcloud.co/v1/universal/taxBandits/latest/actions/list1099-transactions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TaxBandits `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/taxBandits/latest/actions/list1099-transactions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/taxBandits/latest/actions/list1099-transactions?${params}`, {
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
      "Errors": [
        {}
      ],
      "Page": 1,
      "PageSize": 1,
      "TotalPages": 1,
      "TotalRecords": 1,
      "TxnData": [
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
| `Errors` | array<object> |  |
| `Page` | number |  |
| `PageSize` | number |  |
| `TotalPages` | number |  |
| `TotalRecords` | number |  |
| `TxnData` | array<object> |  |

## Native endpoint

Through the native TaxBandits API, this operation is `GET Form1099Transactions` (base URL `https://testapi.taxbandits.com/v1.7.3/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list1099-transactions.md) for the provider-specific parameters and requirements.

