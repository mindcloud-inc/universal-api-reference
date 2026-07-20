# Fiscal Data Service: List Average Interest Rate Records

Retrieves average interest rate records from Fiscal Data Service.

```
GET https://connect.mindcloud.co/v1/universal/fiscalDataService/latest/actions/list-average-interest-rate-records
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fiscal Data Service `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fiscalDataService/latest/actions/list-average-interest-rate-records?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fiscalDataService/latest/actions/list-average-interest-rate-records?${params}`, {
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
      "avg_interest_rate_amt": 1,
      "record_date": "2026-05-07T12:00:00.000Z",
      "security_desc": "string",
      "security_type_desc": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `avg_interest_rate_amt` | number | Average interest rate amount. |
| `record_date` | date | Record date. |
| `security_desc` | string | Security description. |
| `security_type_desc` | string | Security type description. |

## Native endpoint

Through the native Fiscal Data Service API, this operation is `GET /v2/accounting/od/avg_interest_rates` (base URL `https://api.fiscaldata.treasury.gov/services/api/fiscal_service`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-average-interest-rate-records.md) for the provider-specific parameters and requirements.

