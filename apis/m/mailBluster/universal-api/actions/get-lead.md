# MailBluster: Get Lead

Retrieves a lead from MailBluster by lead hash.

```
GET https://connect.mindcloud.co/v1/universal/mailBluster/latest/actions/get-lead
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MailBluster `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mailBluster/latest/actions/get-lead?connectionId=$CONNECTION_ID&leadHash=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "leadHash": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mailBluster/latest/actions/get-lead?${params}`, {
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
| `leadHash` | string | yes | MD5 hash of the lead email. |

## Response

```json
{
  "success": true,
  "data": [
    {
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
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string | Creation timestamp. |
| `email` | string | Lead email address. |
| `fields` | object | Custom field values. |
| `firstName` | string | Lead first name. |
| `fullName` | string | Lead full name. |
| `id` | number | MailBluster lead ID. |
| `ipAddress` | string | Lead IP address when available. |
| `lastName` | string | Lead last name. |
| `meta` | object | Lead metadata. |
| `optInStatus` | string | Opt-in status. |
| `subscribed` | boolean | Whether the lead is subscribed. |
| `tags` | array<string> | Lead tags. |
| `timezone` | string | Lead timezone when available. |
| `updatedAt` | string | Last update timestamp. |

## Native endpoint

Through the native MailBluster API, this operation is `GET /leads/:leadHash` (base URL `https://api.mailbluster.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-lead.md) for the provider-specific parameters and requirements.

