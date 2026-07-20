# Snapchat Lead Generation: List Webhook Integrations

Retrieves webhook integrations for a form in Snapchat Lead Generation.

```
GET https://connect.mindcloud.co/v1/universal/snapchatLeadGeneration/latest/actions/list-webhook-integrations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Snapchat Lead Generation `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/snapchatLeadGeneration/latest/actions/list-webhook-integrations?connectionId=$CONNECTION_ID&formId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "formId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/snapchatLeadGeneration/latest/actions/list-webhook-integrations?${params}`, {
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
| `formId` | string | yes | The Snapchat lead generation form ID whose webhook integrations you want to list. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "partnerIntegrations": [
        {
          "adAccountId": "string",
          "connectionId": "string",
          "genericWebhookHandlerInfo": {
            "webhookUrl": "https://example.com"
          },
          "integrationId": "string",
          "partnerType": "string"
        }
      ],
      "request_id": "string",
      "request_status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `partnerIntegrations[].adAccountId` | string |  |
| `partnerIntegrations[].connectionId` | string |  |
| `partnerIntegrations[].genericWebhookHandlerInfo.webhookUrl` | string |  |
| `partnerIntegrations[].integrationId` | string |  |
| `partnerIntegrations[].partnerType` | string |  |
| `request_id` | string |  |
| `request_status` | string |  |

## Native endpoint

Through the native Snapchat Lead Generation API, this operation is `GET /lead_gen/forms/:formId/integrations` (base URL `https://adsapi.snapchat.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-webhook-integrations.md) for the provider-specific parameters and requirements.

