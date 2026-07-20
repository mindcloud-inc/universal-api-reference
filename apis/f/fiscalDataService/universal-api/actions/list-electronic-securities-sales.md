# Fiscal Data Service: List Electronic Securities Sales

Retrieves electronic securities sales from Fiscal Data Service.

```
GET https://connect.mindcloud.co/v1/universal/fiscalDataService/latest/actions/list-electronic-securities-sales
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fiscal Data Service `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fiscalDataService/latest/actions/list-electronic-securities-sales?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fiscalDataService/latest/actions/list-electronic-securities-sales?${params}`, {
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
      "gross_sales_amt": 1,
      "net_sales_amt": 1,
      "record_date": "2026-05-07T12:00:00.000Z",
      "security_class_desc": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `gross_sales_amt` | number | Gross sales amount. |
| `net_sales_amt` | number | Net sales amount. |
| `record_date` | date | Record date. |
| `security_class_desc` | string | Security class description. |

## Native endpoint

Through the native Fiscal Data Service API, this operation is `GET /v1/accounting/od/securities_sales` (base URL `https://api.fiscaldata.treasury.gov/services/api/fiscal_service`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-electronic-securities-sales.md) for the provider-specific parameters and requirements.

