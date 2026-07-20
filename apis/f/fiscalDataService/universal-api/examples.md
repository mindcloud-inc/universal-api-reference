# Fiscal Data Service Universal API Examples

These examples use the MindCloud API key and Fiscal Data Service connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Debt to the Penny Records

Retrieves Debt to the Penny records from Fiscal Data Service.

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

Example response:

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

See the full [List Debt to the Penny Records action reference](actions/list-debt-to-the-penny-records.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/fiscalDataService/latest/actions/list-debt-to-the-penny-records).
