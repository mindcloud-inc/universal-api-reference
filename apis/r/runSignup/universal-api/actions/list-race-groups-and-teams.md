# RunSignup: List Race Groups and Teams



```
GET https://connect.mindcloud.co/v1/universal/runSignup/latest/actions/list-race-groups-and-teams
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RunSignup `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/runSignup/latest/actions/list-race-groups-and-teams?connectionId=$CONNECTION_ID&raceId=string&eventId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "raceId": "string",
  "eventId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/runSignup/latest/actions/list-race-groups-and-teams?${params}`, {
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
| `eventId` | string | yes | Id of event or list of event ids separated by commas. |
| `modifiedSince` | string | no | Get teams modified on or after a given time. If set, groups are returned in order of last modified date. Otherwise, by group name. |
| `page` | number | no | Page number to get. |
| `resultsPerPage` | number | no | Number of results per page. |
| `includeGroupSizes` | string | no | Include group sizes |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native RunSignup API returns.

## Native endpoint

Through the native RunSignup API, this operation is `GET /race/:race_id/teams` (base URL `https://api.runsignup.com/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-race-groups-and-teams.md) for the provider-specific parameters and requirements.

