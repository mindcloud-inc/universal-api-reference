# Fiscal Data Service: List Title XII Advance Records

Retrieves Title XII advance records from Fiscal Data Service.

```
GET https://connect.mindcloud.co/v1/universal/fiscalDataService/latest/actions/list-title-xii-advance-records
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fiscal Data Service `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fiscalDataService/latest/actions/list-title-xii-advance-records?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fiscalDataService/latest/actions/list-title-xii-advance-records?${params}`, {
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
      "interest_rate_pct": 1,
      "outstanding_advance_bal": 1,
      "record_date": "2026-05-07T12:00:00.000Z",
      "state_nm": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `interest_rate_pct` | number | Interest rate percent. |
| `outstanding_advance_bal` | number | Outstanding advance balance. |
| `record_date` | date | Record date. |
| `state_nm` | string | State or territory name. |

## Native endpoint

Through the native Fiscal Data Service API, this operation is `GET /v2/accounting/od/title_xii` (base URL `https://api.fiscaldata.treasury.gov/services/api/fiscal_service`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-title-xii-advance-records.md) for the provider-specific parameters and requirements.

