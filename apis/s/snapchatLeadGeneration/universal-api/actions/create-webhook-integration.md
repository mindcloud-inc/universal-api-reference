# Snapchat Lead Generation: Create Webhook Integration

Creates a webhook integration in Snapchat Lead Generation.

```
POST https://connect.mindcloud.co/v1/universal/snapchatLeadGeneration/latest/actions/create-webhook-integration
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Snapchat Lead Generation `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/snapchatLeadGeneration/latest/actions/create-webhook-integration" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "webhookIntegrations": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/snapchatLeadGeneration/latest/actions/create-webhook-integration', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "webhookIntegrations": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `webhookIntegrations` | list<object> | yes | An array of webhook integration objects, each containing the Snapchat form ID and the webhook URL to register. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "requestId": "string",
      "requestStatus": "string",
      "webhookIntegrations": [
        {
          "subRequestStatus": "string",
          "webhookIntegration": {
            "adAccountId": "string",
            "formId": "string",
            "hmacSecret": "string",
            "integrationId": "string",
            "partnerType": "string",
            "webhookUrl": "https://example.com"
          }
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `requestId` | string |  |
| `requestStatus` | string |  |
| `webhookIntegrations[].subRequestStatus` | string |  |
| `webhookIntegrations[].webhookIntegration.adAccountId` | string |  |
| `webhookIntegrations[].webhookIntegration.formId` | string |  |
| `webhookIntegrations[].webhookIntegration.hmacSecret` | string |  |
| `webhookIntegrations[].webhookIntegration.integrationId` | string |  |
| `webhookIntegrations[].webhookIntegration.partnerType` | string |  |
| `webhookIntegrations[].webhookIntegration.webhookUrl` | string |  |

## Native endpoint

Through the native Snapchat Lead Generation API, this operation is `POST /lead_gen/integrations/public_webhook` (base URL `https://adsapi.snapchat.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-webhook-integration.md) for the provider-specific parameters and requirements.

