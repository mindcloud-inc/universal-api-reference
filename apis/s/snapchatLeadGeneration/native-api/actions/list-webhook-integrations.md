# List Webhook Integrations with Snapchat Lead Generation

Retrieves webhook integrations for a form in Snapchat Lead Generation.

## Endpoint

- **Method:** `GET`
- **Path:** `/lead_gen/forms/:formId/integrations`
- **Base URL:** `https://adsapi.snapchat.com/v1`
- **Official documentation:** [List Webhook Integrations](https://developers.snap.com/api/marketing-api/Ads-API/lead-generation-ads#get-all-webhook-integrations-under-a-form)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formId` | path | `string` | yes | The Snapchat lead generation form ID whose webhook integrations you want to list. |
