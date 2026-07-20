# MailerLite: Get Subscriber Activity

Retrieves activity for a subscriber in MailerLite.

```
GET https://connect.mindcloud.co/v1/universal/mailerLite/latest/actions/get-subscriber-activity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MailerLite `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mailerLite/latest/actions/get-subscriber-activity?connectionId=$CONNECTION_ID&limit=25&offset=0&id=180863157267334516" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "id": "180863157267334516"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mailerLite/latest/actions/get-subscriber-activity?${params}`, {
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
| `id` | string | yes | Subscriber ID for the account. Example: `180863157267334516`. |
| `filter.logName` | string | no | Activity log type to include. Example: `email_open`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "id": "string",
      "logName": "Ava Chen",
      "subjectId": "string",
      "subjectType": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string |  |
| `id` | string |  |
| `logName` | string |  |
| `subjectId` | string |  |
| `subjectType` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native MailerLite API, this operation is `GET /subscribers/:id/activity-log` (base URL `https://connect.mailerlite.com/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-subscriber-activity.md) for the provider-specific parameters and requirements.

