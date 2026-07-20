# Recommand: Update Webhook

Updates an existing webhook in Recommand.

```
PUT https://connect.mindcloud.co/v1/universal/recommand/latest/actions/update-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Recommand `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/recommand/latest/actions/update-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://example.com",
  "webhookid": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/recommand/latest/actions/update-webhook', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "url": "https://example.com",
    "webhookid": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `companyid` | string | no | companyId body field. |
| `url` | string | yes | url body field. |
| `webhookid` | string | yes | webhookId parameter. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true,
      "webhook": {
        "companyId": "string",
        "createdAt": "string",
        "id": "string",
        "teamId": "string",
        "updatedAt": "string",
        "url": "https://example.com"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean |  |
| `webhook` | object |  |
| `webhook.companyId` | string |  |
| `webhook.createdAt` | string |  |
| `webhook.id` | string |  |
| `webhook.teamId` | string |  |
| `webhook.updatedAt` | string |  |
| `webhook.url` | string |  |

## Native endpoint

Through the native Recommand API, this operation is `PUT /api/v1/webhooks/:webhookId` (base URL `https://app.recommand.eu`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-webhook.md) for the provider-specific parameters and requirements.

