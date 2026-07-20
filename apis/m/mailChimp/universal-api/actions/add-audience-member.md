# Mailchimp: Add Audience Member

Creates a new member in a Mailchimp audience.

```
POST https://connect.mindcloud.co/v1/universal/mailChimp/latest/actions/add-audience-member
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mailchimp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mailChimp/latest/actions/add-audience-member" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email_address": "ava@example.com",
  "list_id": "string",
  "status": "cleaned"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mailChimp/latest/actions/add-audience-member', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email_address": "ava@example.com",
    "list_id": "string",
    "status": "cleaned"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email_address` | string | yes | Subscriber email address. |
| `email_type` | string | no |  |
| `interests` | object | no |  |
| `ip_opt` | string | no |  |
| `ip_signup` | string | no |  |
| `language` | string | no |  |
| `list_id` | string | yes | The unique ID for the Mailchimp audience. |
| `location` | object | no |  |
| `marketing_permissions[]` | array<object> | no |  |
| `merge_fields` | object | no |  |
| `skip_merge_validation` | boolean | no |  |
| `status` | list<string> | yes | Subscription status. One of: `cleaned`, `pending`, `subscribed`, `transactional`, `unsubscribed`. |
| `tags[]` | array<string> | no |  |
| `timestamp_opt` | date | no |  |
| `timestamp_signup` | date | no |  |
| `vip` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "emailAddress": "ava@example.com",
      "emailType": "ava@example.com",
      "fullName": "Ava Chen",
      "id": "string",
      "mergeFields": {},
      "stats": {},
      "status": "string",
      "timestampSignup": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `emailAddress` | string |  |
| `emailType` | string |  |
| `fullName` | string |  |
| `id` | string |  |
| `mergeFields` | object |  |
| `stats` | object |  |
| `status` | string |  |
| `timestampSignup` | date |  |

## Native endpoint

Through the native Mailchimp API, this operation is `POST lists/:list_id/members` (base URL `https://{{credentials.serverPrefix}}.api.mailchimp.com/3.0/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-audience-member.md) for the provider-specific parameters and requirements.

