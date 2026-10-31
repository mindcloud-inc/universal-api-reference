# Bridgit Bench: List Account Person Unavailabilities



```
GET https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/list-account-person-unavailabilities
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bridgit Bench `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/list-account-person-unavailabilities?connectionId=$CONNECTION_ID&accountId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accountId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/list-account-person-unavailabilities?${params}`, {
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
| `accountId` | number | yes | The Account ID |
| `start` | date | no | Date from which to start the range (Default: 0001-01-01) |
| `end` | date | no | Date from which to end the range (Default: 9999-12-31) |
| `boundRange` | boolean | no | Setting this value to true will truncate the dates returned to the specified start and end date paramters Default: `false`. |
| `type` | list<string> | no | Type of the unavailability date range (Default: Unavailability) One of: `All`, `PostEmployment`, `PreEmployment`, `TimeOff`, `Unavailability`. Default: `Unavailability, TimeOff`. |
| `state` | list<string> | no | State of persons to filter results by (Default: Active) One of: `Active`, `All`, `Deactivated`. Default: `Active`. |
| `personIds` | number | no | Optional comma delimited list of person IDs to filter the results if set Accepts multiple values in one string, delimited by `,`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Bridgit Bench API returns.

## Native endpoint

Through the native Bridgit Bench API, this operation is `GET /rp/api/v1/accounts/:accountId/persons/unavailabilities` (base URL `https://bench.gobridgit.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-account-person-unavailabilities.md) for the provider-specific parameters and requirements.

