# Fiscal Data Service: List Debt to the Penny Records

Retrieves Debt to the Penny records from Fiscal Data Service.

```
GET https://connect.mindcloud.co/v1/universal/fiscalDataService/latest/actions/list-debt-to-the-penny-records
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fiscal Data Service `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fiscalDataService/latest/actions/list-debt-to-the-penny-records?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fiscalDataService/latest/actions/list-debt-to-the-penny-records?${params}`, {
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
      "debt_held_public_amt": 1,
      "intragov_hold_amt": 1,
      "record_date": "2026-05-07T12:00:00.000Z",
      "tot_pub_debt_out_amt": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `debt_held_public_amt` | number | Debt held by the public amount. |
| `intragov_hold_amt` | number | Intragovernmental holdings amount. |
| `record_date` | date | Record date. |
| `tot_pub_debt_out_amt` | number | Total public debt outstanding amount. |

## Native endpoint

Through the native Fiscal Data Service API, this operation is `GET /v2/accounting/od/debt_to_penny` (base URL `https://api.fiscaldata.treasury.gov/services/api/fiscal_service`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-debt-to-the-penny-records.md) for the provider-specific parameters and requirements.

