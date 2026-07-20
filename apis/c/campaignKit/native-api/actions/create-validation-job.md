# Create Validation Job with CampaignKit

Creates a bulk email validation job in CampaignKit.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/email/validate/job`
- **Base URL:** `https://api.campaignkit.cc`
- **Official documentation:** [Create Validation Job](https://campaignkit.cc/docs/api/validation-jobs)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `integration` | body | `number` | no | Integration ID when importing contacts from a connected service. |
| `label` | body | `string` | no | Descriptive label for the validation job. |
| `source` | body | `string` | yes | Source type for the validation job: input, file, or excel. Accepted values: `0`, `1`, `2`. |
| `input` | body | `string` | no | Comma-separated or newline-separated email addresses when source is input. |
| `file` | body | `file` | no | CSV or Excel file when source is file or excel. |
