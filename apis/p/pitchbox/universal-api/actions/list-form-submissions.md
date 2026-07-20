# Pitchbox: List Form Submissions



```
GET https://connect.mindcloud.co/v1/universal/pitchbox/latest/actions/list-form-submissions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pitchbox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pitchbox/latest/actions/list-form-submissions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pitchbox/latest/actions/list-form-submissions?${params}`, {
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
      "attemptNumber": 1,
      "id": 1,
      "opportunity": {
        "contactFormUrl": "https://example.com",
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
| `id` | number |  |
| `opportunity.contactFormUrl` | string |  |
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
| `user.displayName` | string |  |
| `user.email` | string |  |
| `user.firstName` | string |  |
| `user.id` | number |  |
| `user.lastName` | string |  |

## Native endpoint

Through the native Pitchbox API, this operation is `GET /api/form_submissions` (base URL `https://apiv2.pitchbox.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-form-submissions.md) for the provider-specific parameters and requirements.

