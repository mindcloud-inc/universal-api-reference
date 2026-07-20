# CPSC Recalls Retrieval Universal API Examples

These examples use the MindCloud API key and CPSC Recalls Retrieval connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Search Recalls

Finds public product recalls in CPSC by search fields.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cPSCRecallsRetrieval/latest/actions/search-recalls?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cPSCRecallsRetrieval/latest/actions/search-recalls?${params}`, {
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
      "ConsumerContact": "string",
      "Description": "string",
      "Distributors": [
        {}
      ],
      "Hazards": [
        {}
      ],
      "Images": [
        {}
      ],
      "Importers": [
        {}
      ],
      "Inconjunctions": [
        {}
      ],
      "Injuries": [
        {}
      ],
      "LastPublishDate": "2026-05-07T12:00:00.000Z",
      "ManufacturerCountries": [
        {}
      ],
      "Manufacturers": [
        {}
      ],
      "Products": [
        {}
      ],
      "ProductUPCs": [
        {}
      ],
      "RecallDate": "2026-05-07T12:00:00.000Z",
      "RecallID": 1,
      "RecallNumber": "string",
      "Remedies": [
        {}
      ],
      "RemedyOptions": [
        {}
      ],
      "Retailers": [
        {}
      ],
      "SoldAtLabel": "string",
      "Title": "string",
      "URL": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Search Recalls action reference](actions/search-recalls.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/cPSCRecallsRetrieval/latest/actions/search-recalls).
