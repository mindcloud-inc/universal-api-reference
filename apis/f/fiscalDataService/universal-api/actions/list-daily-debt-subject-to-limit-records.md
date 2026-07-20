# Fiscal Data Service: List Daily Debt Subject to Limit Records

Retrieves daily debt subject to limit records from Fiscal Data Service.

```
GET https://connect.mindcloud.co/v1/universal/fiscalDataService/latest/actions/list-daily-debt-subject-to-limit-records
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fiscal Data Service `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fiscalDataService/latest/actions/list-daily-debt-subject-to-limit-records?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fiscalDataService/latest/actions/list-daily-debt-subject-to-limit-records?${params}`, {
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
      "close_today_bal": 1,
      "debt_catg": "string",
      "debt_catg_desc": "string",
      "record_date": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `close_today_bal` | number | Closing balance today. |
| `debt_catg` | string | Debt category. |
| `debt_catg_desc` | string | Debt category description. |
| `record_date` | date | Record date. |

## Native endpoint

Through the native Fiscal Data Service API, this operation is `GET /v1/accounting/dts/debt_subject_to_limit` (base URL `https://api.fiscaldata.treasury.gov/services/api/fiscal_service`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-daily-debt-subject-to-limit-records.md) for the provider-specific parameters and requirements.

