# Fiscal Data Service: List Monthly Treasury Security Detail Records

Retrieves monthly Treasury security detail records from Fiscal Data Service.

```
GET https://connect.mindcloud.co/v1/universal/fiscalDataService/latest/actions/list-monthly-treasury-security-detail-records
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fiscal Data Service `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fiscalDataService/latest/actions/list-monthly-treasury-security-detail-records?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fiscalDataService/latest/actions/list-monthly-treasury-security-detail-records?${params}`, {
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
      "current_month_outstanding_amt": 1,
      "record_date": "2026-05-07T12:00:00.000Z",
      "security_class1_desc": "string",
      "security_type_desc": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `current_month_outstanding_amt` | number | Current month outstanding amount. |
| `record_date` | date | Record date. |
| `security_class1_desc` | string | Security class description. |
| `security_type_desc` | string | Security type description. |

## Native endpoint

Through the native Fiscal Data Service API, this operation is `GET /v1/debt/mspd/mspd_table_3` (base URL `https://api.fiscaldata.treasury.gov/services/api/fiscal_service`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-monthly-treasury-security-detail-records.md) for the provider-specific parameters and requirements.

