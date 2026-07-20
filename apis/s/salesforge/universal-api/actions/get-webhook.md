# Salesforge: Get Webhook

Retrieves a webhook from Salesforge.

```
GET https://connect.mindcloud.co/v1/universal/salesforge/latest/actions/get-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Salesforge `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/salesforge/latest/actions/get-webhook?connectionId=$CONNECTION_ID&workspaceId=wks_lxxtq91neaixc8yaiqp7w&webhookId=rwh_9ge03wcb6dokdmxsyv878" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workspaceId": "wks_lxxtq91neaixc8yaiqp7w",
  "webhookId": "rwh_9ge03wcb6dokdmxsyv878"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/salesforge/latest/actions/get-webhook?${params}`, {
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
| `workspaceId` | string | yes | Example: `wks_lxxtq91neaixc8yaiqp7w`. |
| `webhookId` | string | yes | Example: `rwh_9ge03wcb6dokdmxsyv878`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "name": "Ava Chen",
      "sentCount": 1,
      "type": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `name` | string |  |
| `sentCount` | number |  |
| `type` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Salesforge API, this operation is `GET /public/v2/workspaces/:workspaceID/integrations/webhooks/:webhookID` (base URL `https://api.salesforge.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-webhook.md) for the provider-specific parameters and requirements.

