# Fiscal Data Service: List Monthly Receipts Outlays Deficit Surplus

Retrieves monthly receipts and outlays records from Fiscal Data Service.

```
GET https://connect.mindcloud.co/v1/universal/fiscalDataService/latest/actions/list-monthly-receipts-outlays-deficit-surplus
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fiscal Data Service `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fiscalDataService/latest/actions/list-monthly-receipts-outlays-deficit-surplus?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fiscalDataService/latest/actions/list-monthly-receipts-outlays-deficit-surplus?${params}`, {
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
      "amt_category": "string",
      "mil_amt": 1,
      "record_date": "2026-05-07T12:00:00.000Z",
      "record_fiscal_year": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amt_category` | string | Amount category. |
| `mil_amt` | number | Amount in millions. |
| `record_date` | date | Record date. |
| `record_fiscal_year` | number | Fiscal year. |

## Native endpoint

Through the native Fiscal Data Service API, this operation is `GET /v1/accounting/mts/mts_receipts_outlays_deficit_surplus` (base URL `https://api.fiscaldata.treasury.gov/services/api/fiscal_service`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-monthly-receipts-outlays-deficit-surplus.md) for the provider-specific parameters and requirements.

