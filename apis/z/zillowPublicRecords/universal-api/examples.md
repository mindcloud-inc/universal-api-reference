# Zillow Public Records Universal API Examples

These examples use the MindCloud API key and Zillow Public Records connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List assessments

Retrieves public property assessments from Zillow Public Records.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zillowPublicRecords/latest/actions/list-assessments?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zillowPublicRecords/latest/actions/list-assessments?${params}`, {
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
      "address": {},
      "apn": "string",
      "areas": [
        {}
      ],
      "BridgeModificationTimestamp": "2026-05-07T12:00:00.000Z",
      "building": [
        {}
      ],
      "coordinates": [
        1
      ],
      "county": "string",
      "fips": "string",
      "id": "string",
      "improvementValue": 1,
      "landUseCode": "string",
      "landUseDescription": "string",
      "landValue": 1,
      "taxYear": 1,
      "totalValue": 1,
      "zoning": "string"
    }
  ],
  "meta": {}
}
```

See the full [List assessments action reference](actions/list-assessments.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/zillowPublicRecords/latest/actions/list-assessments).
