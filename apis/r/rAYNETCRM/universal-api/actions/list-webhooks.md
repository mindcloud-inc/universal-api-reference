# RAYNET CRM: List Webhooks



```
GET https://connect.mindcloud.co/v1/universal/rAYNETCRM/latest/actions/list-webhooks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RAYNET CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rAYNETCRM/latest/actions/list-webhooks?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rAYNETCRM/latest/actions/list-webhooks?${params}`, {
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
      "entityFilter": [
        "string"
      ],
      "eventsFilter": [
        "string"
      ],
      "name": "Ava Chen",
      "secretToken": "string",
      "url": "https://example.com",
      "webhookId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `entityFilter` | array<string> | Entity filters applied to the webhook. |
| `eventsFilter` | array<string> | Subscribed webhook event types. |
| `name` | string | Webhook display name. |
| `secretToken` | string | Webhook secret token. |
| `url` | string | Webhook destination URL. |
| `webhookId` | string | Raynet webhook identifier. |

## Native endpoint

Through the native RAYNET CRM API, this operation is `GET webhook/` (base URL `https://app.raynetcrm.com/api/v2/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-webhooks.md) for the provider-specific parameters and requirements.

