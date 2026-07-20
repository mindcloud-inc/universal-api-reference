# TaxBandits: Get 1099 Transactions Report

Retrieves a 1099 transactions report from TaxBandits.

```
GET https://connect.mindcloud.co/v1/universal/taxBandits/latest/actions/get1099-transactions-report
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TaxBandits `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/taxBandits/latest/actions/get1099-transactions-report?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/taxBandits/latest/actions/get1099-transactions-report?${params}`, {
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
      "Form1099Txns": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Errors` | array<object> |  |
| `Form1099Txns` | object |  |

## Native endpoint

Through the native TaxBandits API, this operation is `GET Reports/Form1099Transactions` (base URL `https://testapi.taxbandits.com/v1.7.3/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get1099-transactions-report.md) for the provider-specific parameters and requirements.

