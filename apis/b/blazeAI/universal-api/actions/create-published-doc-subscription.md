# Blaze AI: Create Published Doc Subscription

Creates a published document subscription in Blaze AI.

```
POST https://connect.mindcloud.co/v1/universal/blazeAI/latest/actions/create-published-doc-subscription
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Blaze AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/blazeAI/latest/actions/create-published-doc-subscription" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "workspace_id": "994619",
  "hookUrl": "https://example.com/blaze-webhook",
  "subscriptionName": "Codex Temp Subscription"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/blazeAI/latest/actions/create-published-doc-subscription', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "workspace_id": "994619",
    "hookUrl": "https://example.com/blaze-webhook",
    "subscriptionName": "Codex Temp Subscription"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `workspace_id` | number | yes | Default: `994619`. |
| `hookUrl` | string | yes | Default: `https://example.com/blaze-webhook`. |
| `subscriptionName` | string | yes | Default: `Codex Temp Subscription`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "hookUrl": "https://example.com",
        "id": 1,
        "triggerType": "string",
        "workspaceId": 1
      },
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.hookUrl` | string |  |
| `data.id` | number |  |
| `data.triggerType` | string |  |
| `data.workspaceId` | number |  |
| `success` | boolean |  |

## Native endpoint

Through the native Blaze AI API, this operation is `POST /api/v1/w/:workspace_id/published_doc_subscriptions` (base URL `https://api.blaze.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-published-doc-subscription.md) for the provider-specific parameters and requirements.

