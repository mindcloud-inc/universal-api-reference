# RunSignup: List Removed Race Participants



```
GET https://connect.mindcloud.co/v1/universal/runSignup/latest/actions/list-removed-race-participants
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RunSignup `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/runSignup/latest/actions/list-removed-race-participants?connectionId=$CONNECTION_ID&raceId=string&eventId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "raceId": "string",
  "eventId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/runSignup/latest/actions/list-removed-race-participants?${params}`, {
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
| `eventId` | string | yes | ID of event or list of event IDs separated by commas. |
| `page` | number | no | Page number to get. |
| `resultsPerPage` | number | no | Number of results per page. |
| `sort` | string | no | Sort by "registration_id", "registration_date" or "last_modified" in ascending ("ASC") or descending ("DESC") order. |
| `afterRegistrationId` | number | no | Get registrations after the given registration ID. |
| `modifiedAfterTimestamp` | string | no | Get registrations modified on or after a given time. |
| `condensedFormat` | string | no | Use the condensed format, which only includes IDs and the reason for removal from the race. |
| `supportsNb` | string | no | Does integration support non-binary X gender? |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native RunSignup API returns.

## Native endpoint

Through the native RunSignup API, this operation is `GET /race/:race_id/removed-participants` (base URL `https://api.runsignup.com/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-removed-race-participants.md) for the provider-specific parameters and requirements.

