# Fiscal Data Service: List Daily Treasury Operating Cash Balances

Retrieves daily Treasury operating cash balances from Fiscal Data Service.

```
GET https://connect.mindcloud.co/v1/universal/fiscalDataService/latest/actions/list-daily-treasury-operating-cash-balances
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fiscal Data Service `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fiscalDataService/latest/actions/list-daily-treasury-operating-cash-balances?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fiscalDataService/latest/actions/list-daily-treasury-operating-cash-balances?${params}`, {
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
      "account_type": "string",
      "close_today_bal": 1,
      "open_today_bal": 1,
      "record_date": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account_type` | string | Account type. |
| `close_today_bal` | number | Closing balance today. |
| `open_today_bal` | number | Opening balance today. |
| `record_date` | date | Record date. |

## Native endpoint

Through the native Fiscal Data Service API, this operation is `GET /v1/accounting/dts/operating_cash_balance` (base URL `https://api.fiscaldata.treasury.gov/services/api/fiscal_service`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-daily-treasury-operating-cash-balances.md) for the provider-specific parameters and requirements.

