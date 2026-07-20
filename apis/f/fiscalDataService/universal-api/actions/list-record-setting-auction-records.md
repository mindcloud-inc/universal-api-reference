# Fiscal Data Service: List Record Setting Auction Records

Retrieves record-setting auction records from Fiscal Data Service.

```
GET https://connect.mindcloud.co/v1/universal/fiscalDataService/latest/actions/list-record-setting-auction-records
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fiscal Data Service `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fiscalDataService/latest/actions/list-record-setting-auction-records?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fiscalDataService/latest/actions/list-record-setting-auction-records?${params}`, {
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
      "high_rate_pct": 1,
      "low_rate_pct": 1,
      "security_term": "string",
      "security_type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `high_rate_pct` | number | Record high rate percent. |
| `low_rate_pct` | number | Record low rate percent. |
| `security_term` | string | Security term. |
| `security_type` | string | Security type. |

## Native endpoint

Through the native Fiscal Data Service API, this operation is `GET /v2/accounting/od/record_setting_auction` (base URL `https://api.fiscaldata.treasury.gov/services/api/fiscal_service`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-record-setting-auction-records.md) for the provider-specific parameters and requirements.

