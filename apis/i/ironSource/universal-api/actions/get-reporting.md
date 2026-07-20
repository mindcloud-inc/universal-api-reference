# ironSource: Get Reporting

Retrieves reporting data from ironSource.

```
GET https://connect.mindcloud.co/v1/universal/ironSource/latest/actions/get-reporting
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ironSource `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ironSource/latest/actions/get-reporting?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ironSource/latest/actions/get-reporting?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `adFormat` | string | no | Optional ad format filter: rewarded, offerwall, interstitial, or banner. |
| `appKey` | string | no | Optional comma-separated application key filter. |
| `breakdowns` | string | no | Comma-separated breakdown list, defaulting to date when omitted. |
| `country` | string | no | Optional comma-separated ISO 3166-1 alpha-2 country codes. |
| `endDate` | string | no | Report end date in YYYY-MM-DD format, UTC timezone. |
| `metrics` | string | no | Comma-separated metric list, such as revenue,impressions,activeUsers. |
| `startDate` | string | no | Report start date in YYYY-MM-DD format, UTC timezone. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "activeUsers": 1,
      "adFormat": "string",
      "adNetwork": "Ava Chen",
      "app": "Ava Chen",
      "clicks": 1,
      "clickThroughRate": 1,
      "country": "string",
      "date": "2026-05-07T12:00:00.000Z",
      "eCPM": 1,
      "impressions": 1,
      "instance": "string",
      "isBidder": true,
      "mediationAdUnit": "string",
      "mediationGroup": "string",
      "platform": "string",
      "revenue": 1,
      "totalResults": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `activeUsers` | number | Active users count. |
| `adFormat` | string | Ad format breakdown value. |
| `adNetwork` | string | Ad network breakdown value. |
| `app` | string | Application breakdown value. |
| `clicks` | number | Click count. |
| `clickThroughRate` | number | Click-through rate metric. |
| `country` | string | Country breakdown value. |
| `date` | date | Reporting date when date is selected as a breakdown. |
| `eCPM` | number | Effective CPM metric. |
| `impressions` | number | Impression count. |
| `instance` | string | Instance breakdown value. |
| `isBidder` | boolean | Bidder breakdown value. |
| `mediationAdUnit` | string | Mediation ad unit breakdown value. |
| `mediationGroup` | string | Mediation group breakdown value. |
| `platform` | string | Platform breakdown value. |
| `revenue` | number | Revenue metric. |
| `totalResults` | number | Total result count from the reporting envelope. |

## Native endpoint

Through the native ironSource API, this operation is `GET levelPlay/reporting/v1` (base URL `https://platform.ironsrc.com/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-reporting.md) for the provider-specific parameters and requirements.

