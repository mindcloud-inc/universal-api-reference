# RunSignup: List Races



```
GET https://connect.mindcloud.co/v1/universal/runSignup/latest/actions/list-races
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RunSignup `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/runSignup/latest/actions/list-races?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/runSignup/latest/actions/list-races?${params}`, {
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
| `afltToken` | string | no | If set, this affiliate token will be appended to race URLs. |
| `events` | string | no | Includes race events in the output. |
| `raceHeadings` | string | no | Include race headings in the output. |
| `raceLinks` | string | no | Include race links in the output. |
| `includeWaiver` | string | no | Should waiver be included? |
| `includeMultipleWaivers` | string | no | Should multiple waivers be included? |
| `includeEventDays` | string | no | Should information on events days (e.g. each race year) be included? |
| `includeExtraDateInfo` | string | no | Should extra information about cancellations and postponements be included? |
| `includeGiveawayDetails` | string | no | Should detailed giveaway information be included? |
| `page` | number | no | Page number to get. |
| `resultsPerPage` | number | no | Number of results per page. |
| `sort` | string | no | Sort by "name", "date", or "end_date" in ascending ("ASC") or descending ("DESC") order. |
| `name` | string | no | Search by race name. |
| `startDate` | string | no | Searches for races that occur on or after a given date. |
| `endDate` | string | no | Searches for races that occur on or before a given date. |
| `createdSince` | string | no | Searches for races that were created on or after a given date. |
| `createdOnOrBefore` | string | no | Searches for races that were created on or before a given date. |
| `modifiedSince` | string | no | Searches for races that were modified on or after a given date. |
| `modifiedOnOrBefore` | string | no | Searches for races that were modified on or before a given date. |
| `onlyPartnerRaces` | string | no | Only get races linked to the partner using the API. |
| `searchStartDateOnly` | string | no | Only search race races based on start date, not end date. |
| `onlyRacesWithResults` | string | no | Only get races that have results. |
| `city` | string | no | Search by city. |
| `state` | string | no | Search by state. |
| `country` | string | no | Search by country. |
| `eventType` | string | no | Get races by event type. |
| `minDistance` | number | no | Minimum race distance to get. |
| `maxDistance` | number | no | Maximum race distance to get. |
| `distanceUnits` | string | no | Units to use with distance. |
| `zipcode` | string | no | Searches for races within radius(required) miles from zipcode. US Only. |
| `radius` | number | no | Searches for races within radius miles from zipcode(required). |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native RunSignup API returns.

## Native endpoint

Through the native RunSignup API, this operation is `GET /races` (base URL `https://api.runsignup.com/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-races.md) for the provider-specific parameters and requirements.

