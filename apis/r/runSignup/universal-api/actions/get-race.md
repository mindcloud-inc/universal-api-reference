# RunSignup: Get Race



```
GET https://connect.mindcloud.co/v1/universal/runSignup/latest/actions/get-race
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RunSignup `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/runSignup/latest/actions/get-race?connectionId=$CONNECTION_ID&raceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "raceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/runSignup/latest/actions/get-race?${params}`, {
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
| `raceId` | string | yes | Path parameter: race_id |
| `futureEventsOnly` | string | no | Only outputs events that occur in the future. |
| `mostRecentEventsOnly` | string | no | Only outputs most recent events for the race. |
| `raceEventDaysId` | number | no | Get events by race_event_days_id |
| `raceHeadings` | string | no | Include race headings in the output. |
| `raceLinks` | string | no | Include race links in the output. |
| `includeWaiver` | string | no | Should waiver be included? |
| `includeMultipleWaivers` | string | no | Should multiple waivers be included? |
| `includeParticipantCaps` | string | no | Should participant caps be included? |
| `includeAgeBasedPricing` | string | no | Should information on age based pricing be included? |
| `includeGiveawayDetails` | string | no | Should give-away (e.g. T-shirt) details be included? This will include options, such as sizes. |
| `includeQuestions` | string | no | Should questions be included? |
| `includeAddons` | string | no | Should registration add-ons be included? |
| `includeMembershipSettings` | string | no | Should membership settings be included? |
| `includeCorralSettings` | string | no | Should corral settings be included? |
| `includeDonationSettings` | string | no | Should donations settings be included? |
| `includeExtraDateInfo` | string | no | Should extra information about cancellations and postponements be included? |
| `supportsQuestionApplicationTypes` | string | no | Does your integration support question application types? |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native RunSignup API returns.

## Native endpoint

Through the native RunSignup API, this operation is `GET /race/:race_id` (base URL `https://api.runsignup.com/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-race.md) for the provider-specific parameters and requirements.

