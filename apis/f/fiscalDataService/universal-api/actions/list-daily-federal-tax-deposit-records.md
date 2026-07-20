# Fiscal Data Service: List Daily Federal Tax Deposit Records

Retrieves daily federal tax deposit records from Fiscal Data Service.

```
GET https://connect.mindcloud.co/v1/universal/fiscalDataService/latest/actions/list-daily-federal-tax-deposit-records
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fiscal Data Service `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fiscalDataService/latest/actions/list-daily-federal-tax-deposit-records?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fiscalDataService/latest/actions/list-daily-federal-tax-deposit-records?${params}`, {
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
      "record_date": "2026-05-07T12:00:00.000Z",
      "tax_deposit_fytd_amt": 1,
      "tax_deposit_today_amt": 1,
      "tax_deposit_type_desc": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `record_date` | date | Record date. |
| `tax_deposit_fytd_amt` | number | Federal tax deposits fiscal year to date. |
| `tax_deposit_today_amt` | number | Federal tax deposits today. |
| `tax_deposit_type_desc` | string | Federal tax deposit type description. |

## Native endpoint

Through the native Fiscal Data Service API, this operation is `GET /v1/accounting/dts/federal_tax_deposits` (base URL `https://api.fiscaldata.treasury.gov/services/api/fiscal_service`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-daily-federal-tax-deposit-records.md) for the provider-specific parameters and requirements.

