# Tableau Cloud: Get Subscription

Retrieves a subscription from Tableau Cloud.

```
GET https://connect.mindcloud.co/v1/universal/tableauCloud/latest/actions/get-subscription
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tableau Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tableauCloud/latest/actions/get-subscription?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tableauCloud/latest/actions/get-subscription?${params}`, {
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

Through the native Tableau Cloud API, this operation is `GET /sites/site-id/subscriptions/subscription-id` (base URL `https://us-east-1.online.tableau.com/api/3.28`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-subscription.md) for the provider-specific parameters and requirements.

