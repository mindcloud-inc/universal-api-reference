# Fiscal Data Service: List Treasury Gold Reserve Records

Retrieves Treasury gold reserve records from Fiscal Data Service.

```
GET https://connect.mindcloud.co/v1/universal/fiscalDataService/latest/actions/list-treasury-gold-reserve-records
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fiscal Data Service `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fiscalDataService/latest/actions/list-treasury-gold-reserve-records?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fiscalDataService/latest/actions/list-treasury-gold-reserve-records?${params}`, {
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
      "book_value_amt": 1,
      "fine_troy_ounce_qty": 1,
      "location_desc": "string",
      "record_date": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `book_value_amt` | number | Book value amount. |
| `fine_troy_ounce_qty` | number | Fine troy ounce quantity. |
| `location_desc` | string | Gold reserve location description. |
| `record_date` | date | Record date. |

## Native endpoint

Through the native Fiscal Data Service API, this operation is `GET /v2/accounting/od/gold_reserve` (base URL `https://api.fiscaldata.treasury.gov/services/api/fiscal_service`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-treasury-gold-reserve-records.md) for the provider-specific parameters and requirements.

