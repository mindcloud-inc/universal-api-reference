# Get Experiment Details with Zoho PageSense

Retrieves experiment details from Zoho PageSense.

## Endpoint

- **Method:** `GET`
- **Path:** `/portal/:portalName/experiments/:experimentLinkname`
- **Base URL:** `https://pagesense.zoho.com/pagesense/rest/v1`
- **Official documentation:** [Get Experiment Details](https://www.zoho.com/pagesense/developerguide/apidocs/fetchabsplittest.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `portalName` | path | `string` | yes | Portal identifier in the path. |
| `experimentLinkname` | path | `string` | yes | Experiment linkname in the path. |
