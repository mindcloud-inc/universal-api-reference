# Get Agreement Link Submission with Harbour

Retrieves a specific agreement link submission from Harbour.

## Endpoint

- **Method:** `GET`
- **Path:** `https://api.harbourshare.com/v1/agreement_links/:agreement_link_id/submissions/:submission_id`
- **Base URL:** `https://api.myharbourshare.com/v2`
- **Official documentation:** [Get Agreement Link Submission](https://developers.harbourshare.com/#get-agreement-link-submission)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `agreement_link_id` | path | `string` | yes | Agreement link identifier. |
| `submission_id` | path | `string` | yes | Specific submission identifier. |
