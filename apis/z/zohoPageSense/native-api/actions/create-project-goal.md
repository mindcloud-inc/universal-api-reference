# Create Project Goal with Zoho PageSense

Creates a project goal in Zoho PageSense.

## Endpoint

- **Method:** `POST`
- **Path:** `/portal/:portalName/projectgoals/:projectLinkname`
- **Base URL:** `https://pagesense.zoho.com/pagesense/rest/v1`
- **Official documentation:** [Create Project Goal](https://www.zoho.com/pagesense/developerguide/apidocs/creategoals.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `portalName` | path | `string` | yes | Portal identifier in the path. |
| `projectLinkname` | path | `string` | yes | Project linkname in the path. |
| `projectgoal.display_name` | body | `string` | yes | Human-readable goal name. |
| `projectgoal.goal_type` | body | `number` | yes | Goal type code from Zoho PageSense. |
| `projectgoal.project_linkname` | body | `string` | yes | Project linkname inside the request body. |
