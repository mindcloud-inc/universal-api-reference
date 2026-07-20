# Update Experiment Audience with Zoho PageSense

Updates experiment audience settings in Zoho PageSense.

## Endpoint

- **Method:** `PUT`
- **Path:** `https://pagesense.zoho.com/pagesense/api/v1/portal/:portalName/experimentaudience/:experimentLinkname`
- **Base URL:** `https://pagesense.zoho.com/pagesense/rest/v1`
- **Official documentation:** [Update Experiment Audience](https://www.zoho.com/pagesense/developerguide/apidocs/updateexptaudience.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `portalName` | path | `string` | yes | Portal identifier in the path. |
| `experimentLinkname` | path | `string` | yes | Experiment linkname in the path. |
| `experimentaudience` | body | `string` | yes | Audience assignment payload for the experiment. |
