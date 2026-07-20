# Get Project Goals with Zoho PageSense

Retrieves project goals from Zoho PageSense.

## Endpoint

- **Method:** `GET`
- **Path:** `/portal/:portalName/projectgoals/:projectLinkname`
- **Base URL:** `https://pagesense.zoho.com/pagesense/rest/v1`
- **Official documentation:** [Get Project Goals](https://www.zoho.com/pagesense/developerguide/apidocs/fetchgoalsapi.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `portalName` | path | `string` | yes | Portal identifier in the path. |
| `projectLinkname` | path | `string` | yes | Project linkname in the path. |
