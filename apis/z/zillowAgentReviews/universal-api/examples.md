# Zillow Agent Reviews Universal API Examples

These examples use the MindCloud API key and Zillow Agent Reviews connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List reviewees

Retrieves reviewees from Zillow Agent Reviews.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zillowAgentReviews/latest/actions/list-reviewees?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zillowAgentReviews/latest/actions/list-reviewees?${params}`, {
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
      "AccountIdReviewee": "string",
      "AverageReviewRating": 1,
      "BridgeModificationTimestamp": "2026-05-07T12:00:00.000Z",
      "ReviewCount": 1,
      "RevieweeBusinessName": "Ava Chen",
      "RevieweeEmail": "ava@example.com",
      "RevieweeFullName": "Ava Chen",
      "RevieweeKey": "string",
      "RevieweeProfileURL": "https://example.com",
      "RevieweeScreenName": "Ava Chen",
      "RevieweeTitle": "string",
      "ReviewRequestURL": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [List reviewees action reference](actions/list-reviewees.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/zillowAgentReviews/latest/actions/list-reviewees).
