# Recommand: Get Webhook

Retrieves a webhook record from Recommand.

```
GET https://connect.mindcloud.co/v1/universal/recommand/latest/actions/get-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Recommand `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/recommand/latest/actions/get-webhook?connectionId=$CONNECTION_ID&webhookid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "webhookid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/recommand/latest/actions/get-webhook?${params}`, {
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

Through the native Recommand API, this operation is `GET /api/v1/webhooks/:webhookId` (base URL `https://app.recommand.eu`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-webhook.md) for the provider-specific parameters and requirements.

