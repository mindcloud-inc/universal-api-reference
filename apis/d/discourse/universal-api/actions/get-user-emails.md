# Discourse: Get User Emails

Retrieves a Discourse user's email addresses.

```
GET https://connect.mindcloud.co/v1/universal/discourse/latest/actions/get-user-emails
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Discourse `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/discourse/latest/actions/get-user-emails?connectionId=$CONNECTION_ID&username=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "username": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/discourse/latest/actions/get-user-emails?${params}`, {
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
| `username` | string | yes | Discourse username. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "associated_accounts": [
        {}
      ],
      "email": "ava@example.com",
      "secondary_emails": [
        {}
      ],
      "unconfirmed_emails": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `associated_accounts` | array<object> |  |
| `email` | string |  |
| `secondary_emails` | array<object> |  |
| `unconfirmed_emails` | array<object> |  |

## Native endpoint

Through the native Discourse API, this operation is `GET /u/:username/emails.json` (base URL `https://mindcloud.discourse.group`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user-emails.md) for the provider-specific parameters and requirements.

