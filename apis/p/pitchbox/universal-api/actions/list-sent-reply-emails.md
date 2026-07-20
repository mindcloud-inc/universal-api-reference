# Pitchbox: List Sent Reply Emails



```
GET https://connect.mindcloud.co/v1/universal/pitchbox/latest/actions/list-sent-reply-emails
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pitchbox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pitchbox/latest/actions/list-sent-reply-emails?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pitchbox/latest/actions/list-sent-reply-emails?${params}`, {
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
| `sent_at_from` | string | no | Filter sent replies from this date/time. |
| `sent_at_to` | string | no | Filter sent replies up to this date/time. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bcc": "string",
      "cc": "string",
      "emailAccount": {
        "id": 1,
        "name": "ava@example.com"
      },
      "fromEmail": "ava@example.com",
      "fromName": "Ava Chen",
      "id": 1,
      "opportunity": {
        "id": 1,
        "milestone": "string",
        "name": "Ava Chen",
        "url": "https://example.com"
      },
      "project": {
        "id": 1,
        "name": "Ava Chen"
      },
      "scheduleFor": "2026-05-07T12:00:00.000Z",
      "sentAt": "2026-05-07T12:00:00.000Z",
      "stopScheduleOnCommunication": true,
      "subject": "string",
      "toEmail": "ava@example.com",
      "toName": "Ava Chen",
      "user": {
        "displayName": "Ava Chen",
        "email": "ava@example.com",
        "firstName": "Ava",
        "id": 1,
        "lastName": "Chen"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bcc` | string |  |
| `cc` | string |  |
| `emailAccount.id` | number |  |
| `emailAccount.name` | string |  |
| `fromEmail` | string |  |
| `fromName` | string |  |
| `id` | number |  |
| `opportunity.id` | number |  |
| `opportunity.milestone` | string |  |
| `opportunity.name` | string |  |
| `opportunity.url` | string |  |
| `project.id` | number |  |
| `project.name` | string |  |
| `scheduleFor` | date |  |
| `sentAt` | date |  |
| `stopScheduleOnCommunication` | boolean |  |
| `subject` | string |  |
| `toEmail` | string |  |
| `toName` | string |  |
| `user.displayName` | string |  |
| `user.email` | string |  |
| `user.firstName` | string |  |
| `user.id` | number |  |
| `user.lastName` | string |  |

## Native endpoint

Through the native Pitchbox API, this operation is `GET /api/sent_replies` (base URL `https://apiv2.pitchbox.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-sent-reply-emails.md) for the provider-specific parameters and requirements.

