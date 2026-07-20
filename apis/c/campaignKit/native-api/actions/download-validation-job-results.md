# Download Validation Job Results with CampaignKit

Downloads validation job results from CampaignKit as a CSV file.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/email/validate/job/{{id}}/download`
- **Base URL:** `https://api.campaignkit.cc`
- **Official documentation:** [Download Validation Job Results](https://campaignkit.cc/docs/api/validation-jobs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filters[]` | query | `array<string>` | no | Optional classifiers to include in the CSV download. |
| `id` | path | `number` | yes | Validation job ID. |
