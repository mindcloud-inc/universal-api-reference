# Get Validation Job Results with CampaignKit

Retrieves paginated validation job results from CampaignKit.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/email/validate/job/{{id}}/result`
- **Base URL:** `https://api.campaignkit.cc`
- **Official documentation:** [Get Validation Job Results](https://campaignkit.cc/docs/api/validation-jobs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Validation job ID. |
| `pos` | query | `number` | no | Starting position offset for result pagination. |
