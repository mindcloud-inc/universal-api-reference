# City of Tampa, Florida Universal API Examples

These examples use the MindCloud API key and City of Tampa, Florida connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Collection

Retrieves a data collection from City of Tampa, Florida.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cityOfTampaFlorida/latest/actions/get-collection?connectionId=$CONNECTION_ID&collectionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "collectionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cityOfTampaFlorida/latest/actions/get-collection?${params}`, {
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
      "crs": [
        "string"
      ],
      "description": "string",
      "filters": [
        {}
      ],
      "id": "string",
      "itemType": "string",
      "links": [
        {}
      ],
      "title": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Collection action reference](actions/get-collection.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/cityOfTampaFlorida/latest/actions/get-collection).
