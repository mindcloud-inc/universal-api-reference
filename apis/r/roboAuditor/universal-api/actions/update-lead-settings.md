# RoboAuditor: Update Lead Settings



```
PUT https://connect.mindcloud.co/v1/universal/roboAuditor/latest/actions/update-lead-settings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RoboAuditor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/roboAuditor/latest/actions/update-lead-settings" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/roboAuditor/latest/actions/update-lead-settings', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `neverBounce` | number | no | Enable or disable real-time email validation (1 or 0). |
| `emailAddress` | number | no | Enable blocking specific email addresses (1 or 0). |
| `emailDomain` | number | no | Enable blocking specific email domains (1 or 0). |
| `whitelistRadio` | number | no | Enable URL blacklisting (1 or 0). |
| `addEmailAlert` | number | no | Enable email notifications for team members (1 or 0). |
| `whitelistUrls[]` | array<string> | no | Array of URLs to block. |
| `blockEmails[]` | array<string> | no | Array of blocked email addresses. |
| `blockDomains[]` | array<string> | no | Array of blocked email domains. |
| `alertEmails[]` | array<string> | no | Array of emails that receive notifications. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | string | Provider returns an empty response body on successful update. |

## Native endpoint

Through the native RoboAuditor API, this operation is `POST /lead-settings` (base URL `https://app.siteauditor.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-lead-settings.md) for the provider-specific parameters and requirements.

