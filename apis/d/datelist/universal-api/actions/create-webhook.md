# Datelist: Create Webhook

Creates a new webhook in Datelist for booking notifications.

```
POST https://connect.mindcloud.co/v1/universal/datelist/latest/actions/create-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Datelist `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/datelist/latest/actions/create-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://example.com",
  "calendarId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/datelist/latest/actions/create-webhook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "url": "https://example.com",
    "calendarId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `url` | string | yes | The URL Datelist should call for new booking notifications. |
| `calendarId` | number | yes | The Datelist calendar to watch for new bookings. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "calendarId": 1,
      "createdAt": "string",
      "id": 1,
      "updatedAt": "string",
      "url": "https://example.com",
      "userId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `calendarId` | number | Calendar ID. |
| `createdAt` | string | Creation timestamp. |
| `id` | number | Webhook ID. |
| `updatedAt` | string | Update timestamp. |
| `url` | string | Webhook URL. |
| `userId` | number | User ID. |

## Native endpoint

Through the native Datelist API, this operation is `POST /webhooks` (base URL `https://datelist.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-webhook.md) for the provider-specific parameters and requirements.

