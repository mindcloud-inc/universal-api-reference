# Bridgit Bench: List Person Availabilities



```
GET https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/list-person-availabilities
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bridgit Bench `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/list-person-availabilities?connectionId=$CONNECTION_ID&accountId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accountId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/list-person-availabilities?${params}`, {
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
| `relativeDate` | date | no | Optional paramater used to calculate date based properties. If not provided, it is set to today's date in UTC. |
| `start` | date | no | Start date to filter availabilities from (default today UTC) |
| `end` | date | no | End date to filter availabilities to (default 10 years from today UTC) |
| `boundRange` | boolean | no | Setting this value to true will truncate the dates returned to the specified start and end date paramters Default: `true`. |
| `ids` | number | no | Optional paramater of comma delimited ids for filtering results based on the person IDs provided Accepts multiple values in one string, delimited by `,`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `includeUnavailable` | boolean | no | If this is set to true it will return the availabilities and next available dates even if a person doesn't have a next availability. If the person does not have a "nextAvailableDate", then the "availableInDays" property will be -1 Default: `false`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Bridgit Bench API returns.

## Native endpoint

Through the native Bridgit Bench API, this operation is `GET /rp/api/v1/accounts/:accountId/Persons/availabilities` (base URL `https://bench.gobridgit.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-person-availabilities.md) for the provider-specific parameters and requirements.

