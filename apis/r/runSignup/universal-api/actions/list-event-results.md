# RunSignup: List Event Results



```
GET https://connect.mindcloud.co/v1/universal/runSignup/latest/actions/list-event-results
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RunSignup `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/runSignup/latest/actions/list-event-results?connectionId=$CONNECTION_ID&raceId=string&eventId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "raceId": "string",
  "eventId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/runSignup/latest/actions/list-event-results?${params}`, {
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
| `eventId` | number | yes | ID of event. |
| `individualResultSetId` | number | no | ID of result set. |
| `includeTotalFinishers` | string | no | Indicates whether or not to include total finishers in result set metadata. (Not supported for CSV) |
| `includeSplitTimeMs` | string | no | Indicates whether or not to include milliseconds in split times. |
| `modifiedAfterTimestamp` | string | no | Get results modified after a given timestamp |
| `supportsNb` | string | no | Does integration support non-binary X gender? |
| `page` | number | no | Page number to get. |
| `resultsPerPage` | number | no | Number of results per page. |
| `firstName` | string | no | Search for results by first name. |
| `lastName` | string | no | Search for results by last name. |
| `gender` | string | no | Search for results by gender. |
| `bibNum` | number | no | Search for results by bib number. |
| `registrationId` | number | no | Search for results by registration ID. |
| `minPlace` | number | no | Search for results by minimum finishing place. |
| `maxPlace` | number | no | Search for results by maximum finishing place. |
| `minAge` | number | no | Search for results by minimum age. |
| `maxAge` | number | no | Search for results by maximum age. |
| `state` | string | no | Search for results by state. |
| `country` | string | no | Search for results by country. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native RunSignup API returns.

## Native endpoint

Through the native RunSignup API, this operation is `GET /race/:race_id/results/get-results` (base URL `https://api.runsignup.com/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-event-results.md) for the provider-specific parameters and requirements.

