# LinkedIn Ads Reports Universal API Examples

These examples use the MindCloud API key and LinkedIn Ads Reports connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Ad Analytics

Retrieves ad analytics from LinkedIn Ads Reports.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/linkedInAdsReports/latest/actions/get-ad-analytics?connectionId=$CONNECTION_ID&pivot=ACCOUNT&facet=accounts%3DList(urn%253Ali%253AsponsoredAccount%253A123456)&startYear=2026&startMonth=4&startDay=1&endYear=2026&endMonth=4&endDay=26&timeGranularity=DAILY" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "pivot": "ACCOUNT",
  "facet": "accounts=List(urn%3Ali%3AsponsoredAccount%3A123456)",
  "startYear": "2026",
  "startMonth": "4",
  "startDay": "1",
  "endYear": "2026",
  "endMonth": "4",
  "endDay": "26",
  "timeGranularity": "DAILY"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/linkedInAdsReports/latest/actions/get-ad-analytics?${params}`, {
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
      "clicks": 1,
      "comments": 1,
      "costInLocalCurrency": 1,
      "dateRange": {},
      "externalWebsiteConversions": 1,
      "follows": 1,
      "impressions": 1,
      "landingPageClicks": 1,
      "likes": 1,
      "pivotValues": [
        "string"
      ],
      "shares": 1
    }
  ],
  "meta": {}
}
```

See the full [Get Ad Analytics action reference](actions/get-ad-analytics.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/linkedInAdsReports/latest/actions/get-ad-analytics).
