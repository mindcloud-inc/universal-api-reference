# Charidy Universal API Examples

These examples use the MindCloud API key and Charidy connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Campaign

Retrieves a campaign from Charidy.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/charidy/latest/actions/get-campaign?connectionId=$CONNECTION_ID&campaignId=96" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "campaignId": "96"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/charidy/latest/actions/get-campaign?${params}`, {
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
      "attributes": {
        "campaignId": 1,
        "campaignImage": "string",
        "category": "string",
        "currency": "string",
        "currencySign": "string",
        "endDate": "2026-05-07T12:00:00.000Z",
        "mode": 1,
        "shortDescription": "string",
        "shortLink": "https://example.com",
        "startDate": "2026-05-07T12:00:00.000Z",
        "theme": "string",
        "title": "string"
      },
      "id": 1,
      "type": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Campaign action reference](actions/get-campaign.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/charidy/latest/actions/get-campaign).
