# Fiscal Data Service: List Monthly Statutory Debt Limit Records

Retrieves monthly statutory debt limit records from Fiscal Data Service.

```
GET https://connect.mindcloud.co/v1/universal/fiscalDataService/latest/actions/list-monthly-statutory-debt-limit-records
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fiscal Data Service `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fiscalDataService/latest/actions/list-monthly-statutory-debt-limit-records?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fiscalDataService/latest/actions/list-monthly-statutory-debt-limit-records?${params}`, {
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
      "debt_held_public_mil_amt": 1,
      "debt_limit_desc": "string",
      "record_date": "2026-05-07T12:00:00.000Z",
      "total_mil_amt": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `debt_held_public_mil_amt` | number | Debt held by the public in millions. |
| `debt_limit_desc` | string | Debt limit description. |
| `record_date` | date | Record date. |
| `total_mil_amt` | number | Total amount in millions. |

## Native endpoint

Through the native Fiscal Data Service API, this operation is `GET /v1/debt/mspd/mspd_table_2` (base URL `https://api.fiscaldata.treasury.gov/services/api/fiscal_service`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-monthly-statutory-debt-limit-records.md) for the provider-specific parameters and requirements.

