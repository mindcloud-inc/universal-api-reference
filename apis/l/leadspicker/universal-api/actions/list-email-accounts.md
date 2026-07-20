# Leadspicker: List Email Accounts

Retrieves email accounts from Leadspicker.

```
GET https://connect.mindcloud.co/v1/universal/leadspicker/latest/actions/list-email-accounts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Leadspicker `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/leadspicker/latest/actions/list-email-accounts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/leadspicker/latest/actions/list-email-accounts?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "can_edit_reply_to_email": true,
      "daily_sending_limit": 1,
      "email": "ava@example.com",
      "emails_sent_today": 1,
      "from_name": "Ava Chen",
      "has_all_scopes": true,
      "has_failed_sending": true,
      "id": 1,
      "imap_last_error": "string",
      "is_disabled": true,
      "is_limit_reached": true,
      "is_managed": true,
      "is_revoked": true,
      "is_usable": true,
      "labels": [
        {}
      ],
      "provider": "string",
      "reply_to_email": "ava@example.com",
      "signature": {},
      "time_span_followup": "string",
      "time_span_kickoff": "string",
      "user": 1,
      "user_email": "ava@example.com",
      "user_name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `can_edit_reply_to_email` | boolean |  |
| `daily_sending_limit` | number |  |
| `email` | string |  |
| `emails_sent_today` | number |  |
| `from_name` | string |  |
| `has_all_scopes` | boolean |  |
| `has_failed_sending` | boolean |  |
| `id` | number |  |
| `imap_last_error` | string |  |
| `is_disabled` | boolean |  |
| `is_limit_reached` | boolean |  |
| `is_managed` | boolean |  |
| `is_revoked` | boolean |  |
| `is_usable` | boolean |  |
| `labels` | array<object> |  |
| `provider` | string |  |
| `reply_to_email` | string |  |
| `signature` | object |  |
| `time_span_followup` | string |  |
| `time_span_kickoff` | string |  |
| `user` | number |  |
| `user_email` | string |  |
| `user_name` | string |  |

## Native endpoint

Through the native Leadspicker API, this operation is `GET /app/sb/api/email-accounts` (base URL `https://app.leadspicker.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-email-accounts.md) for the provider-specific parameters and requirements.

