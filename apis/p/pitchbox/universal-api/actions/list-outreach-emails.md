# Pitchbox: List Outreach Emails



```
GET https://connect.mindcloud.co/v1/universal/pitchbox/latest/actions/list-outreach-emails
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pitchbox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pitchbox/latest/actions/list-outreach-emails?connectionId=$CONNECTION_ID&sent_at_from=string&sent_at_to=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "sent_at_from": "string",
  "sent_at_to": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pitchbox/latest/actions/list-outreach-emails?${params}`, {
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
| `sent_at_from` | string | yes | Filter outreach emails from this date/time. |
| `sent_at_to` | string | yes | Filter outreach emails up to this date/time. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attemptNumber": 1,
      "bcc": "string",
      "canSpamText": "string",
      "cc": "string",
      "contact": {
        "email": "ava@example.com",
        "firstName": "Ava",
        "id": 1,
        "lastName": "Chen"
      },
      "emailAccount": {
        "id": 1,
        "name": "ava@example.com"
      },
      "fromName": "Ava Chen",
      "id": 1,
      "opportunity": {
        "id": 1,
        "milestone": "string",
        "name": "Ava Chen",
        "project": {
          "id": 1,
          "name": "Ava Chen"
        },
        "url": "https://example.com"
      },
      "reviewType": "string",
      "sentAt": "2026-05-07T12:00:00.000Z",
      "status": "string",
      "subject": "string",
      "toEmail": "ava@example.com",
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
| `attemptNumber` | number |  |
| `bcc` | string |  |
| `canSpamText` | string |  |
| `cc` | string |  |
| `contact.email` | string |  |
| `contact.firstName` | string |  |
| `contact.id` | number |  |
| `contact.lastName` | string |  |
| `emailAccount.id` | number |  |
| `emailAccount.name` | string |  |
| `fromName` | string |  |
| `id` | number |  |
| `opportunity.id` | number |  |
| `opportunity.milestone` | string |  |
| `opportunity.name` | string |  |
| `opportunity.project.id` | number |  |
| `opportunity.project.name` | string |  |
| `opportunity.url` | string |  |
| `reviewType` | string |  |
| `sentAt` | date |  |
| `status` | string |  |
| `subject` | string |  |
| `toEmail` | string |  |
| `user.displayName` | string |  |
| `user.email` | string |  |
| `user.firstName` | string |  |
| `user.id` | number |  |
| `user.lastName` | string |  |

## Native endpoint

Through the native Pitchbox API, this operation is `GET /api/outreach_emails` (base URL `https://apiv2.pitchbox.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-outreach-emails.md) for the provider-specific parameters and requirements.

