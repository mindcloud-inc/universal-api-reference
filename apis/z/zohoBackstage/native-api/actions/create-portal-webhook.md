# Create Portal Webhook with Zoho Backstage

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/portals/:portal_id/webhooks`
- **Base URL:** `https://zohoapis.com/backstage`
- **Official documentation:** [Create Portal Webhook](https://www.zoho.com/backstage/api/v3/create-a-webhook-for-portal.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `portal_id` | path | `string` | yes | The Zoho Backstage portal ID. |
| `action[]` | body | `array<string>` | yes | The webhook event subscriptions. |
| `name` | body | `string` | yes | Webhook display name. |
| `endpoint_url` | body | `string` | yes | Destination URL that receives webhook deliveries. |
