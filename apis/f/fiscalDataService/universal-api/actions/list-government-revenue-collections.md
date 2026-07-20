# Fiscal Data Service: List Government Revenue Collections

Retrieves government revenue collections from Fiscal Data Service.

```
GET https://connect.mindcloud.co/v1/universal/fiscalDataService/latest/actions/list-government-revenue-collections
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fiscal Data Service `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fiscalDataService/latest/actions/list-government-revenue-collections?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fiscalDataService/latest/actions/list-government-revenue-collections?${params}`, {
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
      "channel_type_desc": "string",
      "electronic_category_desc": "string",
      "net_collections_amt": 1,
      "record_date": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `channel_type_desc` | string | Collection channel type description. |
| `electronic_category_desc` | string | Electronic collection category description. |
| `net_collections_amt` | number | Net collections amount. |
| `record_date` | date | Record date. |

## Native endpoint

Through the native Fiscal Data Service API, this operation is `GET /v2/revenue/rcm` (base URL `https://api.fiscaldata.treasury.gov/services/api/fiscal_service`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-government-revenue-collections.md) for the provider-specific parameters and requirements.

