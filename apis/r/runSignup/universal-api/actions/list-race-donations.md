# RunSignup: List Race Donations



```
GET https://connect.mindcloud.co/v1/universal/runSignup/latest/actions/list-race-donations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RunSignup `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/runSignup/latest/actions/list-race-donations?connectionId=$CONNECTION_ID&raceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "raceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/runSignup/latest/actions/list-race-donations?${params}`, {
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
| `page` | number | no | Page number to get. |
| `resultsPerPage` | number | no | Number of results per page. |
| `sinceTs` | number | no | Get donations on or after the provided timestamp. |
| `untilTs` | number | no | Get donations on or before the provided timestamp. |
| `supportsNb` | string | no | Does integration support non-binary X gender? |
| `sortDirection` | string | no | Sort direction based on donation ID ("ASC" or "DESC"). |
| `beforeDonationId` | number | no | Get donations strictly less than the provided ID. |
| `afterDonationId` | number | no | Get donations strictly greater than the provided ID. |
| `includeOnBehalfOfLabels` | string | no | Should on behalf of labels be included? |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native RunSignup API returns.

## Native endpoint

Through the native RunSignup API, this operation is `GET /race/:race_id/donations/list` (base URL `https://api.runsignup.com/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-race-donations.md) for the provider-specific parameters and requirements.

