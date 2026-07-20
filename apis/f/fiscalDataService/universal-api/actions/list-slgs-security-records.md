# Fiscal Data Service: List SLGS Security Records

Retrieves SLGS security records from Fiscal Data Service.

```
GET https://connect.mindcloud.co/v1/universal/fiscalDataService/latest/actions/list-slgs-security-records
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fiscal Data Service `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fiscalDataService/latest/actions/list-slgs-security-records?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fiscalDataService/latest/actions/list-slgs-security-records?${params}`, {
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
      "new_subscriptions_amt": 1,
      "outstanding_0_3_mos_amt": 1,
      "record_date": "2026-05-07T12:00:00.000Z",
      "time_deposit_redemptions_amt": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `new_subscriptions_amt` | number | New subscriptions amount. |
| `outstanding_0_3_mos_amt` | number | Outstanding amount for 0 to 3 months. |
| `record_date` | date | Record date. |
| `time_deposit_redemptions_amt` | number | Time deposit redemptions amount. |

## Native endpoint

Through the native Fiscal Data Service API, this operation is `GET /v1/accounting/od/slgs_securities` (base URL `https://api.fiscaldata.treasury.gov/services/api/fiscal_service`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-slgs-security-records.md) for the provider-specific parameters and requirements.

