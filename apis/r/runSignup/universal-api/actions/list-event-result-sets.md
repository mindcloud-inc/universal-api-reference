# RunSignup: List Event Result Sets



```
GET https://connect.mindcloud.co/v1/universal/runSignup/latest/actions/list-event-result-sets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RunSignup `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/runSignup/latest/actions/list-event-result-sets?connectionId=$CONNECTION_ID&raceId=string&eventId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "raceId": "string",
  "eventId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/runSignup/latest/actions/list-event-result-sets?${params}`, {
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
| `includeTotalFinishers` | string | no | Indicates whether or not to include total finishers in result set metadata. (Not supported for CSV) |
| `includeDivisionFinishers` | string | no | Indicates whether or not to include division finishers in result set metadata. (Not supported for CSV). Division finishers will only be included if include_total_finishers is also set to T. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native RunSignup API returns.

## Native endpoint

Through the native RunSignup API, this operation is `GET /race/:race_id/results/get-result-sets` (base URL `https://api.runsignup.com/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-event-result-sets.md) for the provider-specific parameters and requirements.

