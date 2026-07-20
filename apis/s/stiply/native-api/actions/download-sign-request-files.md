# Download Sign Request Files with Stiply

Downloads Stiply sign request documents as a ZIP file.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/sign_requests/:sign_request/actions/download_files`
- **Base URL:** `https://api.stiply.nl`
- **Official documentation:** [Download Sign Request Files](https://app.stiply.nl/api-documentation/v2#tag/sign-requests/operation/DownloadSignRequestFiles)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sign_request` | path | `number` | yes | Id of the signrequest. |
