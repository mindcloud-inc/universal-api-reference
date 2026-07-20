# Create Webhook Integration with Snapchat Lead Generation

Creates a webhook integration in Snapchat Lead Generation.

## Endpoint

- **Method:** `POST`
- **Path:** `/lead_gen/integrations/public_webhook`
- **Base URL:** `https://adsapi.snapchat.com/v1`
- **Official documentation:** [Create Webhook Integration](https://developers.snap.com/api/marketing-api/Ads-API/lead-generation-ads#create-a-new-webhook-integration)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `webhook_integrations` | body | `list<object>` | yes | An array of webhook integration objects, each containing the Snapchat form ID and the webhook URL to register. |
