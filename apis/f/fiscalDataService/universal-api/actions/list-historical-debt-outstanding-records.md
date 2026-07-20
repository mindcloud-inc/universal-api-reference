# Fiscal Data Service: List Historical Debt Outstanding Records

Retrieves historical debt outstanding records from Fiscal Data Service.

```
GET https://connect.mindcloud.co/v1/universal/fiscalDataService/latest/actions/list-historical-debt-outstanding-records
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fiscal Data Service `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fiscalDataService/latest/actions/list-historical-debt-outstanding-records?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fiscalDataService/latest/actions/list-historical-debt-outstanding-records?${params}`, {
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
      "debt_outstanding_amt": 1,
      "record_calendar_year": 1,
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
| `debt_outstanding_amt` | number | Debt outstanding amount. |
| `record_calendar_year` | number | Calendar year. |
| `record_date` | date | Record date. |
| `record_fiscal_year` | number | Fiscal year. |

## Native endpoint

Through the native Fiscal Data Service API, this operation is `GET /v2/accounting/od/debt_outstanding` (base URL `https://api.fiscaldata.treasury.gov/services/api/fiscal_service`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-historical-debt-outstanding-records.md) for the provider-specific parameters and requirements.

