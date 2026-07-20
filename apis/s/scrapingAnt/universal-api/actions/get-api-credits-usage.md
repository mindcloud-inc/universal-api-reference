# ScrapingAnt: Get API Credits Usage

Retrieves subscription status and API credits from ScrapingAnt.

```
GET https://connect.mindcloud.co/v1/universal/scrapingAnt/latest/actions/get-api-credits-usage
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ScrapingAnt `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapingAnt/latest/actions/get-api-credits-usage?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scrapingAnt/latest/actions/get-api-credits-usage?${params}`, {
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
      "endDate": "2026-05-07T12:00:00.000Z",
      "planName": "Ava Chen",
      "planTotalCredits": 1,
      "remainedCredits": 1,
      "startDate": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `endDate` | date | Subscription period end date. |
| `planName` | string | Current ScrapingAnt subscription plan name. |
| `planTotalCredits` | number | Total API credits included in the current plan period. |
| `remainedCredits` | number | Remaining API credits in the current plan period. |
| `startDate` | date | Subscription period start date. |

## Native endpoint

Through the native ScrapingAnt API, this operation is `GET /usage` (base URL `https://api.scrapingant.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-api-credits-usage.md) for the provider-specific parameters and requirements.

