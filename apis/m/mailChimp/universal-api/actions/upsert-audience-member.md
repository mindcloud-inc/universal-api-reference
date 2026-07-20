# Mailchimp: Upsert Audience Member

Finds a member in Mailchimp, or creates one if no match is found.

```
PUT https://connect.mindcloud.co/v1/universal/mailChimp/latest/actions/upsert-audience-member
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mailchimp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/mailChimp/latest/actions/upsert-audience-member" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email_address": "ava@example.com",
  "list_id": "string",
  "status_if_new": "cleaned",
  "subscriber_hash": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mailChimp/latest/actions/upsert-audience-member', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email_address": "ava@example.com",
    "list_id": "string",
    "status_if_new": "cleaned",
    "subscriber_hash": "string"
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
| `status` | string | no |  |
| `status_if_new` | list<string> | yes | Status to assign when creating a new member. One of: `cleaned`, `pending`, `subscribed`, `transactional`, `unsubscribed`. |
| `subscriber_hash` | string | yes | MD5 hash of the lowercase subscriber email address. |
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

Through the native Mailchimp API, this operation is `PUT lists/:list_id/members/:subscriber_hash` (base URL `https://{{credentials.serverPrefix}}.api.mailchimp.com/3.0/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upsert-audience-member.md) for the provider-specific parameters and requirements.

