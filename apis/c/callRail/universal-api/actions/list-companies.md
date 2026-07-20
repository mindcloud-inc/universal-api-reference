# CallRail: List Companies

Retrieves companies from CallRail.

```
GET https://connect.mindcloud.co/v1/universal/callRail/latest/actions/list-companies
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CallRail `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/callRail/latest/actions/list-companies?connectionId=$CONNECTION_ID&limit=25&offset=0&account_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "account_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/callRail/latest/actions/list-companies?${params}`, {
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
| `account_id` | string | yes | The CallRail account ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "callscoreEnabled": true,
      "callscribeEnabled": true,
      "createdAt": "string",
      "disabledAt": "string",
      "dniActive": "string",
      "formCapture": true,
      "id": "string",
      "keywordSpottingEnabled": "string",
      "leadScoringEnabled": true,
      "name": "Ava Chen",
      "scriptUrl": "https://example.com",
      "status": "string",
      "swapCookieDuration": 1,
      "swapCookieDurationUnit": "string",
      "swapExcludeJquery": "string",
      "swapLandingOverride": "string",
      "swapPpcOverride": "string",
      "timeZone": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `callscoreEnabled` | boolean |  |
| `callscribeEnabled` | boolean |  |
| `createdAt` | string |  |
| `disabledAt` | string |  |
| `dniActive` | string |  |
| `formCapture` | boolean |  |
| `id` | string |  |
| `keywordSpottingEnabled` | string |  |
| `leadScoringEnabled` | boolean |  |
| `name` | string |  |
| `scriptUrl` | string |  |
| `status` | string |  |
| `swapCookieDuration` | number |  |
| `swapCookieDurationUnit` | string |  |
| `swapExcludeJquery` | string |  |
| `swapLandingOverride` | string |  |
| `swapPpcOverride` | string |  |
| `timeZone` | string |  |

## Native endpoint

Through the native CallRail API, this operation is `GET /v3/a/:account_id/companies.json` (base URL `https://api.callrail.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-companies.md) for the provider-specific parameters and requirements.

