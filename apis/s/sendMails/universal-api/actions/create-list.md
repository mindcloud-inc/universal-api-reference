# SendMails: Create List

Creates a new list in SendMails.

```
POST https://connect.mindcloud.co/v1/universal/sendMails/latest/actions/create-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SendMails `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sendMails/latest/actions/create-list" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "fromEmail": "ava@example.com",
  "fromName": "Ava Chen",
  "contact.company": "string",
  "contact.state": "string",
  "contact.address1": "string",
  "contact.address2": "string",
  "contact.city": "string",
  "contact.zip": "string",
  "contact.phone": "string",
  "contact.countryId": "string",
  "contact.email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sendMails/latest/actions/create-list', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "fromEmail": "ava@example.com",
    "fromName": "Ava Chen",
    "contact.company": "string",
    "contact.state": "string",
    "contact.address1": "string",
    "contact.address2": "string",
    "contact.city": "string",
    "contact.zip": "string",
    "contact.phone": "string",
    "contact.countryId": "string",
    "contact.email": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | List name. |
| `fromEmail` | string | yes | Default from email address. |
| `fromName` | string | yes | Default from name. |
| `contact.company` | string | yes | Company name. |
| `contact.state` | string | yes | State, province, or region. |
| `contact.address1` | string | yes | Address line 1. |
| `contact.address2` | string | yes | Address line 2. |
| `contact.city` | string | yes | City. |
| `contact.zip` | string | yes | Zip or postal code. |
| `contact.phone` | string | yes | Phone number. |
| `contact.countryId` | string | yes | Country ID. |
| `contact.email` | string | yes | Contact email address. |
| `contact.url` | string | no | Optional home page URL. |
| `subscribeConfirmation` | string | no | Send subscription confirmation email. |
| `sendWelcomeEmail` | string | no | Send a welcome email. |
| `unsubscribeNotification` | string | no | Send unsubscribe notification to subscribers. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "listUid": "string",
      "message": "string",
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `listUid` | string | UID of the created list. |
| `message` | string | Provider result message. |
| `status` | number | Provider success indicator. |

## Native endpoint

Through the native SendMails API, this operation is `POST /lists` (base URL `https://app.sendmails.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-list.md) for the provider-specific parameters and requirements.

