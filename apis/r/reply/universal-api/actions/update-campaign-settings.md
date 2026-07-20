# Reply: Update Campaign Settings



```
PUT https://connect.mindcloud.co/v1/universal/reply/latest/actions/update-campaign-settings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reply `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/reply/latest/actions/update-campaign-settings" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "campaignId": 1,
  "name": "Ava Chen",
  "settings.dailyThrottling": 1,
  "settings.daysToFinishProspect": 1,
  "settings.disableOpensTracking": true,
  "settings.emailsCountPerDay": 1,
  "settings.emailSendingDelaySeconds": 1,
  "settings.enableLinksTracking": true,
  "settings.repliesHandlingType": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/reply/latest/actions/update-campaign-settings', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "campaignId": 1,
    "name": "Ava Chen",
    "settings.dailyThrottling": 1,
    "settings.daysToFinishProspect": 1,
    "settings.disableOpensTracking": true,
    "settings.emailsCountPerDay": 1,
    "settings.emailSendingDelaySeconds": 1,
    "settings.enableLinksTracking": true,
    "settings.repliesHandlingType": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `campaignId` | number | yes | Reply campaign identifier. |
| `emailAccounts[]` | array<string> | no | Email accounts used to send campaign emails. |
| `name` | string | yes | Campaign name. |
| `settings.dailyThrottling` | number | yes | Prospects processed in a 24-hour period. |
| `settings.daysToFinishProspect` | number | yes | Days taken for a prospect to finish the sequence. |
| `settings.disableOpensTracking` | boolean | yes | Disable email open tracking. |
| `settings.emailsCountPerDay` | number | yes | Maximum emails sent daily. |
| `settings.emailSendingDelaySeconds` | number | yes | Delay between email sends in seconds. |
| `settings.enableLinksTracking` | boolean | yes | Enable click tracking for links. |
| `settings.repliesHandlingType` | string | yes | How Reply handles responses to the campaign. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "emailAccount": "ava@example.com",
      "emailAccounts": [
        "ava@example.com"
      ],
      "id": 1,
      "name": "Ava Chen",
      "scheduleId": 1,
      "settings": {},
      "status": "string",
      "steps": [
        {}
      ],
      "useDefaultEmailAccountFallback": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `emailAccount` | string | Primary sending email account when present. |
| `emailAccounts` | array<string> | Sending email accounts associated with the campaign. |
| `id` | number | Reply campaign identifier. |
| `name` | string | Campaign name. |
| `scheduleId` | number | Reply schedule identifier. |
| `settings` | object | Campaign sending settings returned by Reply. |
| `status` | string | Campaign lifecycle status. |
| `steps` | array<object> | Campaign step definitions returned by Reply. |
| `useDefaultEmailAccountFallback` | boolean | Whether Reply falls back to a default sending account. |

## Native endpoint

Through the native Reply API, this operation is `PATCH /v2/campaigns/:campaignId` (base URL `https://api.reply.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-campaign-settings.md) for the provider-specific parameters and requirements.

