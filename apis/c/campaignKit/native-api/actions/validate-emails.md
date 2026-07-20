# Validate Emails with CampaignKit

Validates one or more email addresses in CampaignKit.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/email/validate`
- **Base URL:** `https://api.campaignkit.cc`
- **Official documentation:** [Validate Emails](https://campaignkit.cc/docs/api/email-validation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `emails[]` | body | `array<string>` | yes | One to one hundred email addresses to validate in a single request. |
