# GoZen DeepAgent: Unregister Webhook

Unregisters a webhook in GoZen DeepAgent.

```
DELETE https://connect.mindcloud.co/v1/universal/goZenDeepAgent/latest/actions/unregister-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoZen DeepAgent `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/goZenDeepAgent/latest/actions/unregister-webhook?connectionId=$CONNECTION_ID&knowledgebaseId=string&integrationId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "knowledgebaseId": "string",
  "integrationId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/goZenDeepAgent/latest/actions/unregister-webhook?${params}`, {
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
| `knowledgebaseId` | string | yes | Chatbot ID. |
| `integrationId` | string | yes | Integration ID in GoZen's database. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "integrationId": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `integrationId` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native GoZen DeepAgent API, this operation is `DELETE /integration/zapierapp/webhook` (base URL `https://api.deepbot.gozen.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/unregister-webhook.md) for the provider-specific parameters and requirements.

