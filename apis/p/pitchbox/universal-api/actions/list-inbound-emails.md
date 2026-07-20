# Pitchbox: List Inbound Emails



```
GET https://connect.mindcloud.co/v1/universal/pitchbox/latest/actions/list-inbound-emails
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pitchbox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pitchbox/latest/actions/list-inbound-emails?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pitchbox/latest/actions/list-inbound-emails?${params}`, {
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
      "createdAt": "2026-05-07T12:00:00.000Z",
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
      "snoozeUntil": "2026-05-07T12:00:00.000Z",
      "status": "string",
      "subject": "string",
      "toEmail": "ava@example.com",
      "toName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
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
| `snoozeUntil` | date |  |
| `status` | string |  |
| `subject` | string |  |
| `toEmail` | string |  |
| `toName` | string |  |

## Native endpoint

Through the native Pitchbox API, this operation is `GET /api/inbound_emails` (base URL `https://apiv2.pitchbox.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-inbound-emails.md) for the provider-specific parameters and requirements.

