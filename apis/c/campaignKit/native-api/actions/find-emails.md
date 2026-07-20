# Find Emails with CampaignKit

Finds professional email addresses in CampaignKit by name and domain.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/email/find`
- **Base URL:** `https://api.campaignkit.cc`
- **Official documentation:** [Find Emails](https://campaignkit.cc/docs/api/email-finder)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `entries[]` | body | `array<object>` | yes | Up to 20 entries with name or firstName/lastName plus domain. |
