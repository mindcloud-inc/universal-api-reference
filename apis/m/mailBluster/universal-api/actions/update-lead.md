# MailBluster: Update Lead

Updates an existing lead in MailBluster by lead hash.

```
PUT https://connect.mindcloud.co/v1/universal/mailBluster/latest/actions/update-lead
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MailBluster `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/mailBluster/latest/actions/update-lead" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "leadHash": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mailBluster/latest/actions/update-lead', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "leadHash": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `leadHash` | string | yes | MD5 hash of the lead email to update. |
| `firstName` | string | no | Updated first name of the lead. |
| `lastName` | string | no | Updated last name of the lead. |
| `subscribed` | boolean | no | Updated subscribed status. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "lead": {
        "createdAt": "string",
        "email": "ava@example.com",
        "fields": {},
        "firstName": "Ava",
        "fullName": "Ava Chen",
        "id": 1,
        "ipAddress": "string",
        "lastName": "Chen",
        "meta": {},
        "optInStatus": "string",
        "subscribed": true,
        "tags": [
          "string"
        ],
        "timezone": "string",
        "updatedAt": "string"
      },
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `lead` | object | Updated lead. |
| `lead.createdAt` | string | Creation timestamp. |
| `lead.email` | string | Lead email address. |
| `lead.fields` | object | Custom field values. |
| `lead.firstName` | string | Lead first name. |
| `lead.fullName` | string | Lead full name. |
| `lead.id` | number | MailBluster lead ID. |
| `lead.ipAddress` | string | Lead IP address when available. |
| `lead.lastName` | string | Lead last name. |
| `lead.meta` | object | Lead metadata. |
| `lead.optInStatus` | string | Opt-in status. |
| `lead.subscribed` | boolean | Whether the lead is subscribed. |
| `lead.tags` | array<string> | Lead tags. |
| `lead.timezone` | string | Lead timezone when available. |
| `lead.updatedAt` | string | Last update timestamp. |
| `message` | string | Operation result message. |

## Native endpoint

Through the native MailBluster API, this operation is `PUT /leads/:leadHash` (base URL `https://api.mailbluster.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-lead.md) for the provider-specific parameters and requirements.

