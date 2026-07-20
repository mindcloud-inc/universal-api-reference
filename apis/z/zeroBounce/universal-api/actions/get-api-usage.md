# ZeroBounce: Get API Usage

Retrieves API usage metrics from ZeroBounce by date range.

```
GET https://connect.mindcloud.co/v1/universal/zeroBounce/latest/actions/get-api-usage
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ZeroBounce `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zeroBounce/latest/actions/get-api-usage?connectionId=$CONNECTION_ID&startDate=2026-03-01&endDate=2026-03-12" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "startDate": "2026-03-01",
  "endDate": "2026-03-12"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zeroBounce/latest/actions/get-api-usage?${params}`, {
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
| `startDate` | string | yes | Start date in yyyy-mm-dd format. Example: `2026-03-01`. |
| `endDate` | string | yes | End date in yyyy-mm-dd format. Example: `2026-03-12`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "endDate": "string",
      "startDate": "string",
      "statusCatchAll": 1,
      "statusDoNotMail": 1,
      "statusInvalid": 1,
      "statusSpamtrap": 1,
      "statusUnknown": 1,
      "statusValid": 1,
      "subStatusAcceptAll": 1,
      "subStatusAliasAddress": 1,
      "subStatusAllowed": 1,
      "subStatusAlternate": 1,
      "subStatusAntispamSystem": 1,
      "subStatusBlocked": 1,
      "subStatusDisposable": 1,
      "subStatusDoesNotAcceptMail": 1,
      "subStatusExceptionOccurred": 1,
      "subStatusFailedSmtpConnection": 1,
      "subStatusFailedSyntaxCheck": 1,
      "subStatusForcibleDisconnect": 1,
      "subStatusGlobalSuppression": 1,
      "subStatusGreylisted": 1,
      "subStatusLeadingPeriodRemoved": 1,
      "subStatusMailboxNotFound": 1,
      "subStatusMailboxQuotaExceeded": 1,
      "subStatusMailServerDidNotRespond": 1,
      "subStatusMailServerTemporaryError": 1,
      "subStatusMxForward": 1,
      "subStatusNoDnsEntries": 1,
      "subStatusPossibleTrap": 1,
      "subStatusPossibleTypo": 1,
      "subStatusRoleBased": 1,
      "subStatusRoleBasedCatchAll": 1,
      "subStatusTimeoutExceeded": 1,
      "subStatusToxic": 1,
      "subStatusUnroutableIpAddress": 1,
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `endDate` | string |  |
| `startDate` | string |  |
| `statusCatchAll` | number |  |
| `statusDoNotMail` | number |  |
| `statusInvalid` | number |  |
| `statusSpamtrap` | number |  |
| `statusUnknown` | number |  |
| `statusValid` | number |  |
| `subStatusAcceptAll` | number |  |
| `subStatusAliasAddress` | number |  |
| `subStatusAllowed` | number |  |
| `subStatusAlternate` | number |  |
| `subStatusAntispamSystem` | number |  |
| `subStatusBlocked` | number |  |
| `subStatusDisposable` | number |  |
| `subStatusDoesNotAcceptMail` | number |  |
| `subStatusExceptionOccurred` | number |  |
| `subStatusFailedSmtpConnection` | number |  |
| `subStatusFailedSyntaxCheck` | number |  |
| `subStatusForcibleDisconnect` | number |  |
| `subStatusGlobalSuppression` | number |  |
| `subStatusGreylisted` | number |  |
| `subStatusLeadingPeriodRemoved` | number |  |
| `subStatusMailboxNotFound` | number |  |
| `subStatusMailboxQuotaExceeded` | number |  |
| `subStatusMailServerDidNotRespond` | number |  |
| `subStatusMailServerTemporaryError` | number |  |
| `subStatusMxForward` | number |  |
| `subStatusNoDnsEntries` | number |  |
| `subStatusPossibleTrap` | number |  |
| `subStatusPossibleTypo` | number |  |
| `subStatusRoleBased` | number |  |
| `subStatusRoleBasedCatchAll` | number |  |
| `subStatusTimeoutExceeded` | number |  |
| `subStatusToxic` | number |  |
| `subStatusUnroutableIpAddress` | number |  |
| `total` | number |  |

## Native endpoint

Through the native ZeroBounce API, this operation is `GET /v2/getapiusage` (base URL `https://api.zerobounce.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-api-usage.md) for the provider-specific parameters and requirements.

