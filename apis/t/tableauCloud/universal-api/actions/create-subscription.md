# Tableau Cloud: Create Subscription

Creates a new subscription in Tableau Cloud.

```
POST https://connect.mindcloud.co/v1/universal/tableauCloud/latest/actions/create-subscription
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tableau Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/tableauCloud/latest/actions/create-subscription" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/tableauCloud/latest/actions/create-subscription', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "attachImage": "string",
      "attachPdf": "string",
      "content": {
        "id": "string",
        "type": "string"
      },
      "id": "string",
      "message": "string",
      "schedule": {
        "frequency": "string",
        "nextRunAt": "string"
      },
      "subject": "string",
      "suspended": "string",
      "user": {
        "id": "string",
        "name": "Ava Chen"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attachImage` | string | Whether an image is attached. |
| `attachPdf` | string | Whether a PDF is attached. |
| `content.id` | string | Subscribed content ID. |
| `content.type` | string | Subscribed content type. |
| `id` | string | Subscription ID. |
| `message` | string | Subscription message. |
| `schedule.frequency` | string | Schedule frequency. |
| `schedule.nextRunAt` | string | Next run timestamp. |
| `subject` | string | Subscription subject. |
| `suspended` | string | Whether the subscription is suspended. |
| `user.id` | string | User ID. |
| `user.name` | string | User name. |

## Native endpoint

Through the native Tableau Cloud API, this operation is `POST /sites/site-id/subscriptions` (base URL `https://us-east-1.online.tableau.com/api/3.28`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-subscription.md) for the provider-specific parameters and requirements.

