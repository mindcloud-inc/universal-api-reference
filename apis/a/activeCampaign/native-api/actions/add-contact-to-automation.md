# Add Contact To Automation with ActiveCampaign

Adds a contact to an automation in ActiveCampaign.

## Endpoint

- **Method:** `POST`
- **Path:** `/contactAutomations`
- **Base URL:** `{apiUrl}/api/3`
- **Official documentation:** [Add Contact To Automation](https://developers.activecampaign.com/reference/create-new-contactautomation)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `contactAutomation` | body | `object` | no |
| `contactAutomation.contact` | body | `number` | yes |
| `contactAutomation.automation` | body | `number` | yes |
