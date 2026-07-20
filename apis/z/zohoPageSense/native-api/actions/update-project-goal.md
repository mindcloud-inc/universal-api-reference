# Update Project Goal with Zoho PageSense

Updates an existing project goal in Zoho PageSense.

## Endpoint

- **Method:** `PUT`
- **Path:** `/portal/:portalName/projectgoals/:projectLinkname`
- **Base URL:** `https://pagesense.zoho.com/pagesense/rest/v1`
- **Official documentation:** [Update Project Goal](https://www.zoho.com/pagesense/developerguide/apidocs/updategoalsapi.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `portalName` | path | `string` | yes | Portal identifier in the path. |
| `projectLinkname` | path | `string` | yes | Project linkname in the path. |
| `projectgoal.display_name` | body | `string` | no | Updated goal display name. |
| `projectgoal.project_linkname` | body | `string` | yes | Project linkname inside the request body. |
