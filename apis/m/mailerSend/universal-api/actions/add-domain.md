# MailerSend: Add Domain



```
POST https://connect.mindcloud.co/v1/universal/mailerSend/latest/actions/add-domain
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MailerSend `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mailerSend/latest/actions/add-domain" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mailerSend/latest/actions/add-domain', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Verified sending domain name to add. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "can": {},
      "dkim": true,
      "domainSettings": {},
      "id": "string",
      "isBeingVerified": true,
      "isCustomLinksAvailable": true,
      "isDnsActive": true,
      "isTrialDomain": true,
      "isVerified": true,
      "name": "Ava Chen",
      "showDkimInfo": true,
      "spf": true,
      "totals": [
        {}
      ],
      "tracking": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `can` | object |  |
| `dkim` | boolean |  |
| `domainSettings` | object |  |
| `id` | string |  |
| `isBeingVerified` | boolean |  |
| `isCustomLinksAvailable` | boolean |  |
| `isDnsActive` | boolean |  |
| `isTrialDomain` | boolean |  |
| `isVerified` | boolean |  |
| `name` | string |  |
| `showDkimInfo` | boolean |  |
| `spf` | boolean |  |
| `totals` | array<object> |  |
| `tracking` | boolean |  |

## Native endpoint

Through the native MailerSend API, this operation is `POST /domains` (base URL `https://api.mailersend.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-domain.md) for the provider-specific parameters and requirements.

