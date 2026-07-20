# Update Experiment Variations with Zoho PageSense

Updates experiment variations in Zoho PageSense.

## Endpoint

- **Method:** `PUT`
- **Path:** `/portal/:portalName/experiments/:experimentLinkname`
- **Base URL:** `https://pagesense.zoho.com/pagesense/rest/v1`
- **Official documentation:** [Update Experiment Variations](https://www.zoho.com/pagesense/developerguide/apidocs/updateabsplittest.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `portalName` | path | `string` | yes | Portal identifier in the path. |
| `experimentLinkname` | path | `string` | yes | Experiment linkname in the path. |
| `experiment` | body | `string` | yes | Experiment object containing variation updates. |
