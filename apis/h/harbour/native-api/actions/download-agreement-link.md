# Download Agreement Link with Harbour

Retrieves downloadable agreement link files from Harbour.

## Endpoint

- **Method:** `GET`
- **Path:** `https://api.harbourshare.com/v1/agreement_links/:agreement_link_id/download`
- **Base URL:** `https://api.myharbourshare.com/v2`
- **Official documentation:** [Download Agreement Link](https://developers.harbourshare.com/#download-agreement-link)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `agreement_link_id` | path | `string` | yes | Unique Harbour agreement link identifier. |
