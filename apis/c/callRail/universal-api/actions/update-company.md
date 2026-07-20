# CallRail: Update Company

Updates a company in CallRail.

```
PUT https://connect.mindcloud.co/v1/universal/callRail/latest/actions/update-company
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CallRail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/callRail/latest/actions/update-company" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "account_id": "string",
  "company_id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/callRail/latest/actions/update-company', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "account_id": "string",
    "company_id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `account_id` | string | yes |  |
| `company_id` | string | yes |  |
| `name` | string | no |  |
| `time_zone` | string | no |  |
| `swap_ppc_override` | boolean | no |  |
| `swap_landing_override` | boolean | no |  |
| `callscribe_enabled` | boolean | no |  |

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

Through the native CallRail API, this operation is `PUT /v3/a/:account_id/companies/:company_id.json` (base URL `https://api.callrail.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-company.md) for the provider-specific parameters and requirements.

