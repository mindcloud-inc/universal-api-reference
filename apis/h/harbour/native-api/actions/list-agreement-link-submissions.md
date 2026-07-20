# List Agreement Link Submissions with Harbour

Retrieves submissions for an agreement link from Harbour.

## Endpoint

- **Method:** `GET`
- **Path:** `https://api.harbourshare.com/v1/agreement_links/:agreement_link_id/submissions`
- **Base URL:** `https://api.myharbourshare.com/v2`
- **Official documentation:** [List Agreement Link Submissions](https://developers.harbourshare.com/#list-agreement-link-submissions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `agreement_link_id` | path | `string` | yes | Agreement link identifier whose submissions you want to list. |
