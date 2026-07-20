# RunSignup: List Race Fundraisers



```
GET https://connect.mindcloud.co/v1/universal/runSignup/latest/actions/list-race-fundraisers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RunSignup `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/runSignup/latest/actions/list-race-fundraisers?connectionId=$CONNECTION_ID&raceId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "raceId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/runSignup/latest/actions/list-race-fundraisers?${params}`, {
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
| `raceId` | number | yes | ID of race. |
| `donationPeriodId` | number | no | Get fundraisers associated with a donation period ID. |
| `num` | number | no | Number of results per page. The allowed range per page is from 1 - 500, outside this range it defaults to 50 per page. |
| `page` | number | no | Number of pages. |
| `modifiedAfterTs` | number | no | Get fundraisers updated after the provided timestamp. |
| `modifiedBeforeTs` | number | no | Get fundraisers updated before the provided timestamp. |
| `includeAmountRaised` | string | no | Get amount raised for fundraisers? |
| `modifiedField` | string | no | Consider only metadata changes or metadata and donation amount changes? Allowed values are 'meta' or 'meta_or_donation'. |
| `includeNumberOfDonations` | string | no | Include number of donations. |
| `includeFundraiserProfileImages` | string | no | Include fundraiser profile image. |
| `includedFundraiserTypes` | string | no | Include fundraisers types. Allowed values: 'any', 'individuals', 'teams' |
| `includeFundraiserTypeInfo` | string | no | Include team fundraiser type info. |
| `includeUmbrellaTeams` | string | no | Include umbrella team info. |
| `includeImportData` | string | no | (Deprecated: Use `include_external_fundraiser_ids` instead.) Include external fundraiser info. |
| `includeExternalFundraiserIds` | string | no | Include external fundraiser info. |
| `includeMinimumCommitmentData` | string | no | Include minimum commitment info. |
| `registrationId` | number | no | Get fundraiser associated with a registration ID. |
| `fundraiserId` | number | no | Get fundraiser associated with a fundraiser ID. |
| `afterFundraiserId` | number | no | Get fundraisers with IDs greater than specified fundraiser ID. |
| `sort` | string | no | Sort by “created_ts”, “last_modified_ts”, “race_fundraiser_id”, or “amount_raised”. |
| `sortDirection` | string | no | Sort direction. Only applicable if `sort` is specified. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native RunSignup API returns.

## Native endpoint

Through the native RunSignup API, this operation is `GET /v2/race-fundraisers/get-race-fundraisers.json` (base URL `https://api.runsignup.com/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-race-fundraisers.md) for the provider-specific parameters and requirements.

