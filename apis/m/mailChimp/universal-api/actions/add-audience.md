# Mailchimp: Add Audience

Creates a new audience in Mailchimp.

```
POST https://connect.mindcloud.co/v1/universal/mailChimp/latest/actions/add-audience
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mailchimp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mailChimp/latest/actions/add-audience" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "permission_reminder": "string",
  "email_type_option": true,
  "contact": {},
  "campaign_defaults": {},
  "contact.company": "string",
  "contact.address1": "string",
  "contact.city": "string",
  "contact.country": "string",
  "campaign_defaults.from_name": "Ava Chen",
  "campaign_defaults.from_email": "ava@example.com",
  "campaign_defaults.subject": "string",
  "campaign_defaults.language": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mailChimp/latest/actions/add-audience', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "permission_reminder": "string",
    "email_type_option": true,
    "contact": {},
    "campaign_defaults": {},
    "contact.company": "string",
    "contact.address1": "string",
    "contact.city": "string",
    "contact.country": "string",
    "campaign_defaults.from_name": "Ava Chen",
    "campaign_defaults.from_email": "ava@example.com",
    "campaign_defaults.subject": "string",
    "campaign_defaults.language": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `double_optin` | boolean | no |  |
| `marketing_permissions` | boolean | no |  |
| `name` | string | yes | Audience name. |
| `notify_on_subscribe` | string | no |  |
| `notify_on_unsubscribe` | string | no |  |
| `use_archive_bar` | boolean | no |  |
| `permission_reminder` | string | yes | Permission reminder shown in footer. |
| `email_type_option` | boolean | yes | Whether users can choose email type. |
| `contact` | object | yes | List contact object. |
| `campaign_defaults` | object | yes | Default campaign sender settings. |
| `contact.company` | string | yes | Company name. |
| `contact.address1` | string | yes | Primary street address. |
| `contact.city` | string | yes | City. |
| `contact.country` | string | yes | Two-letter country code. |
| `campaign_defaults.from_name` | string | yes | Default from name. |
| `campaign_defaults.from_email` | string | yes | Default from email address. |
| `campaign_defaults.subject` | string | yes | Default campaign subject. |
| `campaign_defaults.language` | string | yes | Default campaign language (for example en). |

## Response

```json
{
  "success": true,
  "data": [
    {
      "campaignDefaults": {},
      "contact": {},
      "dateCreated": "2026-05-07T12:00:00.000Z",
      "emailTypeOption": true,
      "id": "string",
      "name": "Ava Chen",
      "permissionReminder": "string",
      "webId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `campaignDefaults` | object |  |
| `contact` | object |  |
| `dateCreated` | date |  |
| `emailTypeOption` | boolean |  |
| `id` | string |  |
| `name` | string |  |
| `permissionReminder` | string |  |
| `webId` | number |  |

## Native endpoint

Through the native Mailchimp API, this operation is `POST lists` (base URL `https://{{credentials.serverPrefix}}.api.mailchimp.com/3.0/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-audience.md) for the provider-specific parameters and requirements.

