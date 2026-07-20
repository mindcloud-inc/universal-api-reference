# RunSignup: List Race Participants



```
GET https://connect.mindcloud.co/v1/universal/runSignup/latest/actions/list-race-participants
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RunSignup `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/runSignup/latest/actions/list-race-participants?connectionId=$CONNECTION_ID&raceId=string&eventId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "raceId": "string",
  "eventId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/runSignup/latest/actions/list-race-participants?${params}`, {
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
| `sort` | string | no | Sort by "registration_id", "registration_date", "age", "name", "first_name", "last_name", "bib_num", "chip_num", "gender" in ascending ("ASC") or descending ("DESC") order. |
| `afterRegistrationId` | number | no | Get registrations after the given registration ID |
| `beforeRegistrationId` | number | no | Get registrations before the given registration ID |
| `modifiedAfterTimestamp` | string | no | Get registrations modified on or after a given time |
| `registeredAfterTimestamp` | string | no | Get registrations registered on or after a given time |
| `registeredBeforeTimestamp` | string | no | Get registrations registered on or before a given time |
| `includeCounties` | string | no | Should the US counties (NOT COUNTRY) be included. |
| `includeTemplateParticipant` | string | no | Should a template participant be included. Registration ID will be -1. |
| `includeUserAnonymousFlag` | string | no | Should the is_anonymous flag be included on users? |
| `includeQuestions` | string | no | Should question responses be included. Ignored for CSV response type. |
| `includeCorrals` | string | no | Should corrals be included. |
| `includeEstFinish` | string | no | Should estimated finish times be included. |
| `includeCorpTeams` | string | no | Should corporate teams be included. |
| `includeRegistrationAddons` | string | no | Should registration add-ons be included. Ignored for CSV response type. |
| `includeMemberships` | string | no | Should registration memberships be included. Ignored for CSV response type. |
| `includeCouponDetails` | string | no | Should coupon details be included. |
| `includeRegistrationNotes` | string | no | Should registration notes be included. |
| `includeCheckinData` | string | no | Should checkin data be included. |
| `includeWaiverInfo` | string | no | Should waiver info be included. |
| `includeMultipleWaivers` | string | no | Should info for multiple waivers be included? |
| `includeUsatWaiverInfo` | string | no | Should USAT waiver info be included. |
| `includePendingLotterySelection` | string | no | Should pending lottery selection participants be included. |
| `excludeRegistrationsViaSuperEvent` | string | no | Exclude event registrations that are due to the registrant signing up for a super event that includes this event. |
| `includeShippingAddress` | string | no | Should shipping address be included (if enabled). |
| `includeProfileType` | string | no | Should profile type be included. |
| `includeProfileImageUrl` | string | no | Should profile image URLs be included. |
| `supportsNb` | string | no | Does integration support non-binary X gender? |
| `includeFundraisers` | string | no | Should fundraiser and team fundraiser information be included? |
| `includeMultiRaceBundleInfo` | string | no | Should multi-race bundle information be included? |
| `includeTransferredParticipants` | string | no | Should transferred participants be included? |
| `searchFirstName` | string | no | Search for users by first name. |
| `searchLastName` | string | no | Search for users by last name. |
| `searchEmail` | string | no | Search for users by email address. |
| `searchBib` | number | no | Search for users by bib number. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native RunSignup API returns.

## Native endpoint

Through the native RunSignup API, this operation is `GET /race/:race_id/participants` (base URL `https://api.runsignup.com/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-race-participants.md) for the provider-specific parameters and requirements.

